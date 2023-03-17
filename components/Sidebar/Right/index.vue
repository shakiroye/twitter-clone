<template>
  <div class="flex flex-col">
    <!-- Preview Card: what's happening -->
    <SidebarRightPreviewCard title="What's happening">
      <SidebarRightPreviewCardItem v-for="whatHappening in whatHappeningItems">
        <div class="">
          <h2 class="font-bold text-gray-800 text-md dark:text-white">
            {{ whatHappening.title }}
          </h2>
          <p class="text-xs text-gray-400">
            {{ whatHappening.count }}
          </p>
        </div>
      </SidebarRightPreviewCardItem>
    </SidebarRightPreviewCard>

    <!-- Preview Card: Who to follow -->
    <SidebarRightPreviewCard title="Who to follow">
      <SidebarRightPreviewCardItem v-for="whoToFollow in whoToFollowItems">
        <div class="flex flex-row justify-between items-center p-2">
          <div class="flex flex-row">
            <img
              :src="whoToFollow.image"
              :alt="whoToFollow.name"
              class="w-10 h-10 rounded-full"
            />

            <div class="flex flex-col ml-2">
              <h1 class="text-sm font-bold text-gray-900 dark:text-white">
                {{ whoToFollow.name }}
              </h1>
              <p class="text-xs text-gray-400">{{ whoToFollow.handle }}</p>
            </div>
          </div>

          <div class="flex h-full">
            <button
              class="px-4 py-2 font-bold text-xs text-white dark:text-black bg-black dark:bg-white rounded-full"
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
const whatHappeningItems = ref([
  {
    title: "SpaceX",
    count: "18.8k Tweets",
  },
  {
    title: "#CodingIsFun",
    count: "9.3k Tweets",
  },
  {
    title: "#ArtForAll",
    count: "3.5k Tweets",
  },
]);

const whoToFollowItems = ref([
  {
    name: "Shakir OYEOSSI",
    handle: "@shakiroye",
    image: "https://picsum.photos/200/200",
  },
  {
    name: "Shakir OYEOSSI",
    handle: "@shakiroye",
    image: "https://picsum.photos/200/200",
  },
  {
    name: "Shakir OYEOSSI",
    handle: "@shakiroye",
    image: "https://picsum.photos/200/200",
  },
]);
</script>

<style lang="scss" scoped></style>
