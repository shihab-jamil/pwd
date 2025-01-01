<template>
  <div class="flex items-center justify-between border-b-2 border-red-500 py-2 text-sm text-gray-500">
    <!-- Tabs -->
    <div class="flex space-x-8  ">
      <button
          v-for="(tab, index) in tabs"
          :key="index"
          @click="activeTab = index"
          class="flex items-center space-x-1 font-medium focus:outline-none"
          :class="{
          'text-red-500': activeTab === index,
          'text-gray-500 hover:text-gray-400': activeTab !== index,
        }"
      >
        <Icon
            :icon="tab.icon"
            width="24"
            height="24"
            :class="{
              'text-red-500': activeTab === index,
              'text-gray-500': activeTab !== index,
            }"
        />
        <span class="text-lg">{{ tab.name }}</span>
      </button>
    </div>

    <!-- View More -->
    <div>
      <a href="#" class="text-red-500 hover:underline flex items-center text-lg">
        View more <span class="ml-1"><Icon icon="mdi:arrow-right" width="24" height="24" /></span>
      </a>
    </div>
  </div>

  <div class="p-4 text-gray-300">
    <div v-if="activeTab === 0">
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 p-5">
        <card
          title="TUCKER 2022 port to 2k24"
          submitted-by="Robert KiddOX"
          platform="2k24"
          views="129"
          downloads="232"
        >
          <template #card-img>
            <img
                src="~/assets/card/image 6.png"
                alt="Card Image"
                class="w-full h-48 object-cover"
            />
          </template>
        </card>
        <card
            title="TUCKER 2022 port to 2k24"
            submitted-by="Robert KiddOX"
            platform="2k24"
            views="129"
            downloads="232"
        >
          <template #card-img>
            <img
              src="~/assets/card/image 6-2.png"
              alt="Card Image"
              class="w-full h-48 object-cover"
            />
          </template>
        </card>
        <card
            title="TUCKER 2022 port to 2k24"
            submitted-by="Robert KiddOX"
            platform="2k24"
            views="129"
            downloads="232"
        >
          <template #card-img>
            <img
                src="~/assets/card/image 6-4.png"
                alt="Card Image"
                class="w-full h-48 object-cover"
            />
          </template>
        </card>
        <card
            title="TUCKER 2022 port to 2k24"
            submitted-by="Robert KiddOX"
            platform="2k24"
            views="129"
            downloads="232"
        >
          <template #card-img>
            <img
                src="~/assets/card/image 6-1.png"
                alt="Card Image"
                class="w-full h-48 object-cover"
            />
          </template>
        </card>
        <card
            title="TUCKER 2022 port to 2k24"
            submitted-by="Robert KiddOX"
            platform="2k24"
            views="129"
            downloads="232"
        >
          <template #card-img>
            <img
                src="~/assets/card/image 6-3.png"
                alt="Card Image"
                class="w-full h-48 object-cover"
            />
          </template>
        </card>
        <card
            title="TUCKER 2022 port to 2k24"
            submitted-by="Robert KiddOX"
            platform="2k24"
            views="129"
            downloads="232"
        >
          <template #card-img>
            <img
                src="~/assets/card/image 6-5.png"
                alt="Card Image"
                class="w-full h-48 object-cover"
            />
          </template>
        </card>
      </div>
    </div>
    <div v-else-if="activeTab === 1">
      <p class="text-white">📈 Here’s the content for "Trending".</p>
    </div>
    <div v-else-if="activeTab === 2">
      <p class="text-white">❤️ Content for "Popular" goes here.</p>
    </div>
    <div v-else-if="activeTab === 3">
      <p class="text-white">🎲 This is the content for "Random".</p>
    </div>
    <div v-else-if="activeTab === 4">
      <p class="text-white">⏳ Content for "Coming Soon" is displayed here.</p>
    </div>
  </div>
</template>

<script setup>

// Tabs Data
const tabs = [
  { name: "What's Hot", icon: "mdi:fire" },
  { name: "Trending", icon: "gg:trending" },
  { name: "Popular", icon: "iconamoon:heart-bold" },
  { name: "Random", icon: "fad:random-1dice" },
  { name: "Coming Soon", icon: "hugeicons:coming-soon-02" },
];

const activeTab = ref(0); // Tracks the active tab
</script>
