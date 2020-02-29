<template>
    <div class="h-48 flex-1 bg-white hover:bg-gradient-teal-love text-gray-700 hover:text-white shadow-md hover:shadow-teal-love rounded-xl mx-2 p-5 flex items-end">
        <div>
            <svg-icon
                    :name="cardData.icon"
                    class="h-12 w-12 fill-current mb-2"
            />
            <p class="tracking-wider text-xs">{{cardData.label}}</p>
            <p class="text-xl font-bold tracking-wider">{{cardData.value}}</p>
        </div>
    </div>
</template>

<script>
    import SvgIcon from "@/components/SVG"

    export default {
        props: {
            cardData: Object
        },
        components: {
            SvgIcon
        }
    }
</script>
