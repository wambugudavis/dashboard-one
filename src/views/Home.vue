<template>
    <div class="min-h-screen bg-gray-100 flex w-full text-sm text-left">
        <div class="w-full md:w-4/5 flex flex-row">
            <div class="w-1/12 hidden md:block relative">
                <navigation/>
            </div>
            <div class="w-full md:w-11/12 pt-4">
                <div class="px-6 py-4">
                    <button class="round-style bg-gradient-teal-love shadow-teal-love float-right text-white">
                        finish sprint
                    </button>
                    <div class="flex flex-row items-center">
                        <svg-icon
                                name="ArrowLeft"
                                class="h-5 mr-3 fill-current text-gray-300"
                        />
                        <svg-icon
                                name="ArrowRight"
                                class="h-5 fill-current text-gray-500"
                        />
                    </div>
                </div>
                <div class="px-6 py-4 flex flex-row">
                    <h1 class="text-xl font-bold text-gray-700">Sprint Overview</h1>
                    <span class="round-style ml-6 bg-white shadow text-gray-500">Last Sprint</span>
                </div>
                <div class="px-6 py-4 flex flex-col md:flex-row -mx-0 md:-mx-4">
                    <overview-card
                            v-for="(card, index) in overviewData"
                            :key="index"
                            :card-data="card"
                            class="my-2"
                    />
                </div>
                <div class="px-6 py-4 flex flex-col md:flex-row">
                    <div class="flex-1 flex flex-col">
                        <div class="flex flex-row">
                            <h1 class="text-xl font-bold text-gray-700">Burndown chart</h1>
                            <h1 class="text-xl text-gray-400 ml-6">Burnup chart</h1>
                        </div>
                        <div class="bg-white shadow-md h-full py-6 px-8 mr-0 md:mr-4 my-4 rounded-xl">
                            <graph
                                    class="h-56"
                            />
                        </div>
                    </div>
                    <div class="flex-1 flex flex-col">
                        <div class="flex flex-row ml-4 pt-4 md:pt-0">
                            <h1 class="text-xl font-bold text-gray-700">Sprint stories</h1>
                            <span class="round-style bg-white shadow-md text-gray-500 ml-auto">See All</span>
                        </div>
                        <div class="ml-4 my-4 flex flex-col">
                            <sprint-story
                                    :storyData="sprintStories"
                            />
                        </div>
                    </div>
                </div>
                <div class="px-6 py-4 flex">
                    <div class="flex-1 flex flex-col">
                        <h1 class="text-xl font-bold text-gray-700">Team Members</h1>
                        <div class="flex flex-col md:flex-row">
                            <div class="w-full md:w-10/12 bg-white shadow-md h-full py-4 px-6 -mr-8 my-4 z-10 rounded-xl">
                                <member
                                        :members="members"
                                />
                            </div>
                            <div class="w-full md:w-2/12 bg-teal-love shadow-md h-full py-2 px-6 text-right my-4 text-white rounded-xl cursor-pointer">
                                <div class="flex flex-row md:flex-col items-center justify-center md:justify-start p-4 md:p-0">
                                    <span class="mr-1 md:mr-0">Add new</span>
                                    <span>member</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="w-1/5 hidden md:block">
            <sidebar/>
        </div>
    </div>
</template>

<script>
    import Sidebar from '@/components/Sidebar'
    import Navigation from '@/components/Navigation'
    import SvgIcon from "@/components/SVG"
    import OverviewCard from "@/components/OverviewCard"
    import SprintStory from "@/components/SprintStory"
    import Member from "@/components/Member"
    import Graph from "@/components/Graph"

    export default {
        name: 'Home',
        components: {
            Sidebar,
            Navigation,
            SvgIcon,
            OverviewCard,
            SprintStory,
            Member,
            Graph
        },
        data: () => {
            return {
                overviewData: [
                    {
                        icon: 'TrendingUp',
                        label: 'Team velocity',
                        value: 52
                    },
                    {
                        icon: 'User',
                        label: 'Team members',
                        value: 12
                    },
                    {
                        icon: 'Notification',
                        label: 'Tasks delivered',
                        value: 23
                    },
                    {
                        icon: 'Graph',
                        label: 'Spikes delivered',
                        value: 16
                    },
                    {
                        icon: 'Cog',
                        label: 'New events',
                        value: 15
                    },
                ],
                sprintStories: [
                    {
                        id: 'P42',
                        story: 'Onboarding',
                        status: 'Delivered',
                        tasks: 3
                    },
                    {
                        id: 'P32',
                        story: 'User profile',
                        status: 'Delivered',
                        tasks: 8
                    },
                    {
                        id: 'P56',
                        story: 'Landing page',
                        status: 'PO Approval',
                        tasks: 12
                    },
                    {
                        id: 'P36',
                        story: 'Settings',
                        status: 'PO Approval',
                        tasks: 9
                    },
                    {
                        id: 'P67',
                        story: 'New template',
                        status: 'Delivered',
                        tasks: 16
                    }
                ],
                members: [
                    {
                        id: 11,
                        name: 'Jack',
                        points: 50,
                        active: false
                    },
                    {
                        id: 12,
                        name: 'Manny',
                        points: 30,
                        active: true
                    },
                    {
                        id: 13,
                        name: 'Henry',
                        points: 15,
                        active: false
                    },
                    {
                        id: 14,
                        name: 'Jan',
                        points: 98,
                        active: true
                    },
                    {
                        id: 15,
                        name: 'Ann',
                        points: 12,
                        active: false
                    }
                ]
            }
        }
    }
</script>
