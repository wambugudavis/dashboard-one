<template>
    <div class="min-h-screen bg-gray-100 flex w-full text-sm text-left">
        <div class="w-4/5 flex flex-row">
            <div class="w-1/12 relative">
                <navigation/>
            </div>
            <div class="w-11/12 pt-4">
                <div class="px-6 py-4">
                    <button class="round-style bg-gradient-teal-love shadow-teal-love float-right text-white">
                        Button
                    </button>
                </div>
                <div class="px-6 py-4 flex flex-row">
                    <h1 class="text-xl font-bold text-gray-700">Sprint Overview</h1>
                    <span class="round-style ml-6 bg-white shadow text-gray-500">Last Sprint</span>
                </div>
                <div class="px-6 py-4 flex flex-row -mx-4">
                    <div
                            v-for="(n, index) in 5"
                            :key="index"
                            class="h-48 flex-1 bg-white hover:bg-gradient-teal-love text-gray-700 hover:text-white shadow-md hover:shadow-teal-love rounded-xl mx-2 p-5 flex items-end">
                        <div>
                            <p class="tracking-wider text-xs">Team Velocity</p>
                            <p class="text-xl font-bold tracking-wider">52</p>
                        </div>
                    </div>
                </div>
                <div class="px-6 py-4 flex flex-row">
                    <div class="flex-1 flex flex-col">
                        <div class="flex flex-row">
                            <h1 class="text-xl font-bold text-gray-700">Burndown chart</h1>
                            <h1 class="text-xl text-gray-400 ml-6">Burnup chart</h1>
                        </div>
                        <div class="bg-white shadow-md h-full p-6 mr-4 my-4 rounded-xl">

                        </div>
                    </div>
                    <div class="flex-1 flex flex-col">
                        <div class="flex flex-row ml-4">
                            <h1 class="text-xl font-bold text-gray-700">Sprint stories</h1>
                            <span class="round-style bg-white shadow-md text-gray-500 ml-auto">See All</span>
                        </div>
                        <div class="ml-4 my-4 flex flex-col">
                            <div v-for="(n, index) in 6"
                                 :key="index"
                                 class="flex flex-row text-xs px-4 py-3 rounded-lg hover:shadow-md hover:bg-white cursor-pointer"
                            >
                                <span class="w-2/12 uppercase text-gray-500 tracking-wide">P42</span>
                                <span class="w-4/12 text-gray-700 tracking-wide">Onboarding</span>
                                <span class="w-3/12 text-gray-700 tracking-wide">Delivered</span>
                                <span class="w-2/12 text-gray-700 tracking-wide">3</span>
                                <span class="w-1/12 text-gray-700 tracking-wide">...</span>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="px-6 py-4 flex">
                    <div class="flex-1 flex flex-col">
                        <h1 class="text-xl font-bold text-gray-700">Team Members</h1>
                        <div class="flex flex-row">
                            <div class="w-10/12 bg-white shadow-md h-full py-4 px-6 -mr-8 my-4 z-10 rounded-xl flex flex-row items-center">
                                <div
                                        v-for="(n, index) in 5"
                                        :key="index"
                                        class="w-1/5 px-4 flex flex-row items-center">
                                    <div class="relative active-profile">
                                        <img src="https://www.fillmurray.com/640/360"
                                             class="rounded-full h-12 w-12 object-center object-cover" alt="">
                                        <span class="absolute right-0 -mt-3 mr-1 border-2 border-white bg-teal-love rounded-full absolute shadow-teal-love"></span>
                                    </div>
                                    <div class="ml-4 flex flex-col">
                                        <span class="text-gray-700 text-xs font-semibold">Name</span>
                                        <span class="text-gray-400 text-xs font-semibold">50 points</span>
                                    </div>
                                </div>
                            </div>
                            <div class="w-2/12 bg-teal-love shadow-md h-full py-2 px-6 text-right my-4 text-white rounded-xl">
                                <div class="flex flex-col items-center">
                                    <span>Add new</span>
                                    <span>member</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="w-1/5">
            <sidebar/>
        </div>
    </div>
</template>

<script>
    import Sidebar from '@/components/Sidebar'
    import Navigation from '@/components/Navigation'

    export default {
        name: 'Home',
        components: {
            Sidebar,
            Navigation
        }
    }
</script>
