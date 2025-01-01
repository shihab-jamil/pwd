<template>
  <div class="max-w-sm mb-8 bg-[#1F1F1F] text-white rounded-lg overflow-hidden shadow-lg shadow-red-500 relative">
    <!-- Image -->
    <slot name="card-img" />


    <!-- Card Content -->
    <div class="p-4">
      <h2 class="text-lg font-semibold mb-2">{{ title }}</h2>
      <p class="text-sm text-gray-400 mb-1">
        Submitted by <span class="text-white font-semibold">{{ submittedBy }}</span>
      </p>
      <p class="text-sm text-gray-400">
        Platform - <span class="text-red-500 font-semibold">{{ platform }}</span>
      </p>
    </div>

    <!-- Footer Stats -->
    <div
        class="flex justify-between items-center px-4 py-4 text-gray-400 text-sm"
    >
      <div class="flex items-center space-x-1">
        <!-- Eye Icon -->
        <Icon icon="hugeicons:view" class="text-red-500" width="24" height="24" />
        <span>{{ views }}</span>
      </div>

      <div class="flex items-center space-x-1">
        <!-- Eye Off Icon -->
        <Icon icon="mingcute:download-3-line" class="text-red-500" width="24" height="24" />
        <span>{{ downloads }}</span>
      </div>
    </div>
  </div>

</template>

<script setup>
const props = defineProps({
  title : {
    type: String,
    required: true
  },
  submittedBy : {
    type: String,
    required: true
  },
  platform : {
    type: String,
    required: true
  },
  views : {
    type : String,
    required: true
  },
  downloads : {
    type: String,
    required: true
  }
})
</script>