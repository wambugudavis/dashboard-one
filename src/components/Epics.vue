<template>
    <div>
        <div v-for="(epic, index) in epicsData" :key="index" class="py-3 flex flex-row w-full items-center cursor-pointer">
            <div class="w-4/5 flex flex-row items-center">
                <div
                        class="epic-badge"
                        :class="`bg-${epic.color}-200 text-${epic.color}-900`"
                >{{epic.badge}}
                </div>
                <div class="text-xs">
                    <p class="text-gray-800 font-semibold">{{epic.label}}</p>
                    <p class="text-gray-500">{{epic.type}}</p>
                </div>
            </div>
            <div class="w-1/5">
                <span class="float-right">...</span>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            epicsData: Array
        }
    }
</script>
