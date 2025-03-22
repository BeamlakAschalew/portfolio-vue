<script setup>
import { Github, Linkedin, Mail } from 'lucide-vue-next'

defineProps({
  navItems: {
    type: Array,
    required: true,
  },
})
</script>

<template>
  <footer class="mt-16 border-t-4 border-black bg-gray-100">
    <div class="mx-auto max-w-7xl p-6 md:p-8">
      <div class="flex flex-col items-center justify-between gap-6 md:flex-row">
        <!-- Logo -->
        <div
          class="rotate-2 border-4 border-black bg-yellow-400 px-4 py-2 font-black uppercase shadow-[4px_4px_0px_0px_rgba(0,0,0,1)]"
        >
          <span class="text-xl">Beamlak</span>
        </div>

        <!-- Copyright -->
        <div class="text-center">
          <p
            class="inline-block -rotate-1 border-2 border-black bg-white px-4 py-2 font-bold shadow-[2px_2px_0px_0px_rgba(0,0,0,1)]"
          >
            {{ new Date().getFullYear() }} | Built using Vuejs 💚.
          </p>
        </div>

        <!-- Social Icons -->
        <div class="flex gap-3">
          <a
            href="https://github.com/BeamlakAschalew"
            class="h-10 w-10 flex items-center justify-center rotate-1 border-2 border-black bg-white shadow-[2px_2px_0px_0px_rgba(0,0,0,1)] transition-all hover:rotate-0 hover:bg-gray-100"
          >
            <Github class="h-5 w-5" />
          </a>
          <a
            href="https://et.linkedin.com/in/beamlak-aschalew-a0866622b"
            class="h-10 w-10 flex items-center justify-center -rotate-1 border-2 border-black bg-white shadow-[2px_2px_0px_0px_rgba(0,0,0,1)] transition-all hover:rotate-0 hover:bg-gray-100"
          >
            <Linkedin class="h-5 w-5" />
          </a>
          <a
            href="mailto:beamlakaschalew.19@gmail.com"
            class="h-10 w-10 flex items-center justify-center rotate-2 border-2 border-black bg-white shadow-[2px_2px_0px_0px_rgba(0,0,0,1)] transition-all hover:rotate-0 hover:bg-gray-100"
          >
            <Mail class="h-5 w-5" />
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>
