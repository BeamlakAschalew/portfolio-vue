<script setup>
import { Github, ArrowUpRight } from 'lucide-vue-next'

defineProps({
  title: String,
  description: String,
  imageUrl: String,
  tags: Array,
  codeLink: String,
  demoLink: String,
})
</script>

<template>
  <div
    class="group relative transform border-4 border-black bg-yellow-300 shadow-[8px_8px_0px_0px_rgba(0,0,0,1)] transition-all hover:-rotate-1 hover:shadow-[12px_12px_0px_0px_rgba(0,0,0,1)]"
  >
    <!-- Image container -->
    <div class="relative h-48 overflow-hidden border-b-4 border-black md:h-64">
      <img
        :src="imageUrl"
        :alt="title"
        class="h-full w-full object-cover transition-transform duration-500 group-hover:scale-110"
      />
    </div>

    <!-- Content -->
    <div class="p-6">
      <h3 class="mb-2 text-2xl font-black">{{ title }}</h3>
      <p class="mb-4 font-medium">{{ description }}</p>

      <!-- Tags -->
      <div class="mb-6 flex flex-wrap gap-2">
        <span
          v-for="(tag, index) in tags"
          :key="index"
          class="rotate-1 border-2 border-black bg-white px-2 py-1 text-sm font-bold shadow-[2px_2px_0px_0px_rgba(0,0,0,1)]"
        >
          {{ tag }}
        </span>
      </div>

      <!-- Actions -->
      <div class="flex gap-3">
        <a
          :href="codeLink"
          target="_blank"
          class="flex-1 flex items-center justify-center border-2 border-black bg-white font-bold text-black shadow-[4px_4px_0px_0px_rgba(0,0,0,1)] transition-all hover:bg-gray-100 hover:shadow-[6px_6px_0px_0px_rgba(0,0,0,1)] py-2"
        >
          <Github class="mr-2 h-5 w-5" />
          Code
        </a>
        <a
          v-if="demoLink"
          :href="demoLink"
          target="_blank"
          class="flex-1 flex items-center justify-center border-2 border-black bg-black font-bold text-white shadow-[4px_4px_0px_0px_rgba(0,0,0,1)] transition-all hover:bg-gray-900 hover:shadow-[6px_6px_0px_0px_rgba(0,0,0,1)] py-2"
        >
          <ArrowUpRight class="mr-2 h-5 w-5" />
          Link
        </a>
      </div>
    </div>
  </div>
</template>
