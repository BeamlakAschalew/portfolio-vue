<script setup>
defineProps({
  skills: {
    type: Array,
    required: true,
  },
})
</script>

<template>
  <div class="p-6 md:p-8" id="skills">
    <h2
      class="mb-8 mt-20 inline-block -rotate-1 border-4 border-black bg-white px-6 py-2 text-3xl font-black uppercase shadow-[6px_6px_0px_0px_rgba(0,0,0,1)] md:text-4xl"
    >
      Skills & Technologies
    </h2>

    <div class="grid gap-6 md:grid-cols-2 lg:grid-cols-3">
      <div
        v-for="(skill, index) in skills"
        :key="skill.name"
        :class="`transform border-4 border-black ${skill.color} p-6 shadow-[8px_8px_0px_0px_rgba(0,0,0,1)] transition-all hover:shadow-[12px_12px_0px_0px_rgba(0,0,0,1)] ${index % 2 === 0 ? 'rotate-1' : '-rotate-1'}`"
      >
        <div class="mb-4 flex items-center gap-3">
          <div class="rounded-full border-4 border-black bg-white p-2">
            <component :is="skill.icon" class="h-8 w-8" />
          </div>
          <h3 class="text-2xl font-black">{{ skill.name }}</h3>
        </div>

        <ul class="space-y-2">
          <li v-for="item in skill.items" :key="item" class="flex items-center gap-2">
            <span class="inline-block h-3 w-3 rounded-sm bg-black"></span>
            <span class="font-bold">{{ item }}</span>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
