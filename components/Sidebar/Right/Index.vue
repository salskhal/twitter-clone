<template>
  <div class="flex flex-col">
    <!-- Preview Card : Happening -->
    <SidebarRightPreviewCard title="Trends for you">
      <SidebarRightPreviewCardItem
        v-for="(whatsHappening, index) in whatsHappeningItems"
        :key="index"
      >
        <div>
          <h2 class="font-bold text-gray-800 text-md dark:text-white">
            {{ whatsHappening.title }}
          </h2>
          <p class="text-xs text-gray-400">
            {{ whatsHappening.count }}
          </p>
        </div>
      </SidebarRightPreviewCardItem>
    </SidebarRightPreviewCard>

    <!-- Preview Card: Who to follow -->
    <SidebarRightPreviewCard title="Who to follow">
      <SidebarRightPreviewCardItem
        v-for="(whoToFollow, index) in whoToFollowItems"
        :key="index"
      >
        <div class="flex flex-row justify-between items-center p-2">
          <div class="flex flex-row">
            <img class="w-10 h-10 rounded-full" :src="whoToFollow.img" alt="" />
            <div class="flex flex-col ml-2">
              <h1 class="text-sm font-bold text-gray-900 dark:text-white">
                {{ whoToFollow.name }}
              </h1>
              <p class="text-xs text-gray-400">{{ whoToFollow.handle }}</p>
            </div>
          </div>

          <div class="flex h-full">
            <button
              class="px-4 py-2 text-xs font-bold text-white bg-black dark:text-black dark:bg-white rounded-full"
            >
              Follow
            </button>
          </div>
        </div>
      </SidebarRightPreviewCardItem>
    </SidebarRightPreviewCard>
  </div>
</template>

<script setup>
const whatsHappeningItems = ref([
  {
    title: "Bola Ahmed Tinubu",
    count: "20.2k Tweets",
  },
  {
    title: "#Obidient",
    count: "2k Tweets",
  },
  {
    title: "#Batified",
    count: "40.2k Tweets",
  },
  {
    title: "#Next-Level",
    count: "10.2k Tweets",
  },
]);

const whoToFollowItems = ref([
  {
    name: "Mukhtar Salman",
    handle: "@lil-sal",
    img: "https://picsum.photos/200/200",
  },
  {
    name: "Mukhtar Salman",
    handle: "@lil-sal",
    img: "https://picsum.photos/200/200",
  },
]);
</script>
