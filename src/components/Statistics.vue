<template>
    <div>
        <div v-for="(data, index) in statistics" :key="index" class="py-2 flex flex-row w-full">
            <div class="bg-gray-200 py-3 px-4 rounded-xl-left w-full flex flex-row items-center">
                <div class="w-1/3">
                    <span class="font-bold text-gray-90">{{data.description}}</span>
                </div>
                <div class="w-1/3 flex justify-center items-center">
                    <span class="font-semibold text-gray-400 text-xl">{{data.coverage}}</span>
                    <small class="font-thin text-gray-400">%</small>
                </div>
                <div class="w-1/3 font-light">{{data.status}}</div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data: () => {
            return {
                statistics: [
                    {
                        description: 'Project progress',
                        coverage: 75,
                        status: 'precent'
                    },
                    {
                        description: 'Business goals',
                        coverage: 42,
                        status: 'delivered'
                    },
                    {
                        description: 'Budget used',
                        coverage: 42,
                        status: 'precent'
                    }
                ]
            }
        }
    }
</script>
