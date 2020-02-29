<template>
    <div class="relative">
        <div class="bg-white shadow-lg h-screen fixed w-1/5 pt-4">
            <div class="py-4 px-6">
                <div class="">
                    <span class="round-style bg-white shadow-md text-gray-500 float-right">See All</span>
                    <h1 class="text-xl font-bold text-gray-700">Epics</h1>
                    <div class="py-4">
                        <epics
                                :epics-data="epicsData"
                        />
                    </div>
                </div>
                <div class="">
                    <h1 class="text-xl font-bold text-gray-700">Project statistic</h1>
                    <div class="py-2 -mr-6">
                        <statistics/>
                        <div class="pt-4">
                            <span class="round-style bg-white shadow-md text-gray-500">Project Details</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import Epics from '@/components/Epics'
    import Statistics from '@/components/Statistics'

    export default {
        data: () => {
            return {
                epicsData: [
                    {
                        badge: 'O',
                        color: 'green',
                        label: 'Mobile Onboarding',
                        type: 'Design'
                    },
                    {
                        badge: 'G',
                        color: 'red',
                        label: 'Development',
                        type: 'Design'
                    },
                    {
                        badge: 'B',
                        color: 'purple',
                        label: 'Admin panel',
                        type: 'Design & development'
                    }
                ]
            }
        },
        components: {
            Epics, Statistics
        }
    }
</script>
