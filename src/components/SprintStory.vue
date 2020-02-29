<template>
    <div>
        <div
                v-for="(story, index) in storyData"
                :key="index"
                class="flex flex-row items-center text-xs px-4 py-3 rounded-lg hover:shadow-md hover:bg-white cursor-pointer"
        >
            <span class="w-2/12 uppercase text-gray-500 tracking-wide">{{story.id}}</span>
            <span class="w-3/12 text-gray-700 tracking-wide font-thin">{{story.story}}</span>
            <div class="w-4/12 text-gray-700 tracking-wide font-thin flex flex-row items-center">
                <span class="h-1 w-1 bg-teal-love rounded-full mx-2"></span>
                {{story.status}}
            </div>
            <span class="w-2/12 text-gray-700 tracking-wide">{{story.tasks}}</span>
            <span class="w-1/12 text-gray-700 tracking-wide font-semibold text-lg">...</span>
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            storyData: Array
        }
    }
</script>
