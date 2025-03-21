<script setup>
defineProps({
  techStack: {
    type: Array,
    required: true,
  },
})
</script>

<template>
  <section class="p-6 md:p-8">
    <h2
      class="mb-8 inline-block -rotate-1 border-4 border-black bg-white px-6 py-2 text-3xl font-black uppercase shadow-[6px_6px_0px_0px_rgba(0,0,0,1)] md:text-4xl"
    >
      Tech Stack
    </h2>

    <div class="flex flex-wrap gap-4">
      <div
        v-for="tech in techStack"
        :key="tech.name"
        :class="`inline-block transform ${tech.rotate} border-4 border-black ${tech.color} px-4 py-2 font-black shadow-[4px_4px_0px_0px_rgba(0,0,0,1)] transition-all hover:shadow-[6px_6px_0px_0px_rgba(0,0,0,1)]`"
      >
        {{ tech.name }}
      </div>
    </div>
  </section>
</template>
