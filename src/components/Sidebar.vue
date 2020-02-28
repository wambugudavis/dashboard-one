<template>
    <div class="relative">
        <div class="bg-white shadow-lg h-screen fixed w-1/5 pt-4">
            <div class="py-4 px-6">
                <div class="">
                    <span class="round-style bg-white shadow-md text-gray-500 float-right">See All</span>
                    <h1 class="text-xl font-bold text-gray-700">Epics</h1>
                    <div class="py-4">
                        <div v-for="(n, index) in 3" :key="index" class="py-3 flex flex-row w-full items-center">
                            <div class="w-4/5 flex flex-row items-center">
                                <div class="epic-badge bg-red-200 text-red-900">0</div>
                                <div class="text-xs">
                                    <p class="text-gray-800 font-semibold">Mobile Onboarding</p>
                                    <p class="text-gray-500">Design</p>
                                </div>
                            </div>
                            <div class="w-1/5">
                                <span class="float-right">...</span>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="">
                    <h1 class="text-xl font-bold text-gray-700">Project statitic</h1>
                    <div class="py-2 -mr-6">
                        <div v-for="(n, index) in 3" :key="index" class="py-2 flex flex-row w-full">
                            <div class="bg-gray-200 py-3 px-4 rounded-xl-left w-full flex flex-row items-center">
                                <div class="w-1/3">
                                    <span class="font-bold text-gray-90">Project progress</span>
                                </div>
                                <div class="w-1/3">

                                </div>
                                <div class="w-1/3 font-light">delivered</div>
                            </div>
                        </div>
                        <div class="pt-4">
                            <span class="round-style bg-white shadow-md text-gray-500">Project Details</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
