<template>
    <div class="bg-white shadow-lg h-screen fixed w-20 flex justify-center">
        <div class="py-6 px-3 flex flex-col">
            <div class="flex items-center" style="height: 70vh">
                <div>
                    <div v-for="(link, index) in links" :key="index"
                         class="h-10 w-10 my-8 rounded-full hover:text-white hover:shadow-teal-love hover:bg-gradient-teal-love flex items-center justify-center"
                         :class="{
                         'text-white shadow-teal-love bg-gradient-teal-love': link.active,
                         'text-gray-500': !link.active
                         }"
                    >
                        <svg-icon
                                :name="link.icon"
                                class="fill-current"
                        />
                    </div>
                </div>
            </div>
            <div class="flex-1 flex flex-col items-end">
                <div class="h-10 w-10 my-8 rounded-full text-gray-500 hover:text-white hover:shadow-teal-love hover:bg-gradient-teal-love flex items-center justify-center">
                    <svg-icon
                            name="Notification"
                            class="fill-current"
                    />
                </div>
                <div class="relative">
                    <img src="https://i.pravatar.cc/300"
                         class="rounded-full h-10 w-10 object-center object-cover mx-auto" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import SvgIcon from "@/components/SVG"

    export default {
        data: () => {
            return {
                links: [
                    {
                        icon: 'Plus',
                        active: true
                    },
                    {
                        icon: 'Grid',
                        active: false
                    },
                    {
                        icon: 'Menu',
                        active: false
                    },
                    {
                        icon: 'Graph',
                        active: false
                    },
                    {
                        icon: 'Cog',
                        active: false
                    }
                ]
            }
        },
        components: {
            SvgIcon
        }
    }
</script>
