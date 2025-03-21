<script setup>
defineProps({
  education: {
    type: Array,
    required: true,
  },
})
</script>

<template>
  <section class="p-6 md:p-8" id="education">
    <h2
      class="mb-8 inline-block rotate-1 border-4 border-black bg-white px-6 py-2 text-3xl font-black uppercase shadow-[6px_6px_0px_0px_rgba(0,0,0,1)] md:text-4xl"
    >
      Education
    </h2>

    <div class="mx-auto max-w-4xl">
      <div
        v-for="(item, index) in education"
        :key="index"
        class="mb-8 gap-10 flex flex-col md:flex-row"
      >
        <!-- Year -->
        <div class="mb-4 md:mb-0 md:w-1/4">
          <div
            :class="`inline-block rotate-2 transform border-4 border-black ${item.color} px-4 py-2 text-xl font-black shadow-[4px_4px_0px_0px_rgba(0,0,0,1)]`"
          >
            {{ item.year }}
          </div>
        </div>

        <!-- Content -->
        <div class="md:w-3/4">
          <div
            class="-rotate-1 transform border-4 border-black bg-white p-6 shadow-[8px_8px_0px_0px_rgba(0,0,0,1)] transition-all hover:shadow-[12px_12px_0px_0px_rgba(0,0,0,1)]"
          >
            <h3 class="mb-2 text-xl font-black">{{ item.title }}</h3>
            <p class="font-medium">{{ item.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
