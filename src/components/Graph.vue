<script>
    import {Line} from "vue-chartjs";

    export default {
        extends: Line,
        data() {
            return {
                gradient: null
            };
        },
        mounted() {
            this.gradient = this.$refs.canvas
                .getContext("2d")
                .createLinearGradient(0, 0, 0, 450);

            this.gradient.addColorStop(0, "rgba(17,255,189,0.7)");
            this.gradient.addColorStop(0.05, "rgba(17,255,189,0.5)");
            this.gradient.addColorStop(0.4, "rgba(17,255,189,0)");

            this.renderChart(
                {
                    labels: [
                        'x', 'x', 'x', 'x', 'x', 'x', 'x', 'x', 'x', 'x', 'x', 'x', 'x', 'x'
                    ],
                    datasets: [
                        {
                            label: "Data One",
                            borderColor: "#11FFBD",
                            borderWidth: 4,
                            pointBorderColor: "white",
                            backgroundColor: this.gradient,
                            data: [47, 50, 40, 35, 25, 25, 35, 33, 20, 30, 29, 25, 46, 40]
                        }
                    ]
                },
                {
                    responsive: true,
                    maintainAspectRatio: false,
                    legend: {
                        display: false
                    },
                    showLine: true,
                    elements: {
                        point: {
                            radius: 0
                        },
                        lineTension: 0.1
                    },
                    scales: {
                        xAxes: [{
                            gridLines: {
                                display: false,
                                drawBorder: false,
                            },
                            ticks: {
                                display: false,
                                drawBorder: false
                            }
                        }],
                        yAxes: [{
                            gridLines: {
                                drawBorder: false,
                            },
                            ticks: {
                                padding: 10,
                                beginAtZero: true,
                                stepSize: 10,
                                fontColor: "lightGray",
                                fontSize: 10,
                                max: 60
                            }
                        }]
                    }
                }
            );
        }
    };
</script>
