<template>
    <div class="flex flex-col">
        <SidebarRightPreviewCard title="What's happening">
            <SidebarRightPreviewCardItem v-for="item in whatsHappeningItems">
                <h2 class="font-bold text-gray-800 text-md dark:text-white">{{ item.title }}</h2>
                <p class="text-xs text-gray-400">{{ item.count }}</p>
            </SidebarRightPreviewCardItem>
        </SidebarRightPreviewCard>
        <SidebarRightPreviewCard title="Who to follow">
            <SidebarRightPreviewCardItem v-for="item in whoToFollowItems">
                <div class="flex flex-row justify-between p-2">
                    <div class="flex flex-row">
                        <img class="w-10 h-10 rounded-full" :src="item.image" :alt="item.name">
                        <div class="flex flex-col ml-2">
                            <h1 class="text-sm font-bold text-gray-900 dark:text-white">{{ item.name }}</h1>
                            <p class="text-xs text-gray">{{ item.username }}</p>
                        </div>
                    </div>
                    <div class="flex h-full">
                        <button class="px-4 py-2 font-bold text-xs text-white dark:text-black bg-black dark:bg-white rounded-full">Follow</button>
                    </div>
                </div>
            </SidebarRightPreviewCardItem>
        </SidebarRightPreviewCard>
    </div>
</template>

<script setup>
const whatsHappeningItems = ref([
    {
        title: "SpaceX",
        count: "18.8k Tweets"
    },
    {
        title: "Trump",
        count: "12.8k Tweets"
    },
    {
        title: "Elon Musk",
        count: "8.8k Tweets"
    }
])

const whoToFollowItems = ref([
    {
        name: "Donald Trump",
        username: "@realDonaldTrump",
        image: "https://www.usnews.com/object/image/00000187-3996-d0b6-a7e7-b9f67e3a0000/ap23064025376604.jpg?update-time=1680298477110&size=responsive640"
    },
    {
        name: "Donald Trump",
        username: "@realDonaldTrump",
        image: "https://www.usnews.com/object/image/00000187-3996-d0b6-a7e7-b9f67e3a0000/ap23064025376604.jpg?update-time=1680298477110&size=responsive640"
    }
])
</script>