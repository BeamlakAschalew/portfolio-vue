<template>
  <header class="sticky top-0 z-50 border-b-4 border-black bg-white">
    <div class="mx-auto flex max-w-7xl items-center justify-between p-4">
      <!-- Logo -->
      <div
        class="rotate-2 border-4 border-black bg-yellow-400 px-4 py-2 font-black uppercase shadow-[4px_4px_0px_0px_rgba(0,0,0,1)]"
      >
        <span class="text-xl">Beamlak</span>
      </div>

      <!-- Desktop Navigation -->
      <nav class="hidden md:block">
        <ul class="flex items-center gap-2">
          <li v-for="item in navItems" :key="item.name">
            <a
              :href="item.href"
              class="inline-block border-2 border-transparent px-4 py-2 font-bold transition-all hover:rotate-2 hover:border-black hover:bg-black hover:text-white hover:shadow-[4px_4px_0px_0px_rgba(0,0,0,1)]"
            >
              {{ item.name }}
            </a>
          </li>
        </ul>
      </nav>

      <!-- Mobile Menu Button -->
      <button @click="toggleMenu" class="border-2 border-black p-2 md:hidden">
        <X v-if="isMenuOpen" class="h-6 w-6" />
        <Menu v-else class="h-6 w-6" />
      </button>
    </div>

    <!-- Mobile Navigation -->
    <transition name="menu">
      <nav v-show="isMenuOpen" class="border-t-4 border-black bg-white md:hidden">
        <ul class="flex flex-col">
          <li v-for="item in navItems" :key="item.name">
            <a
              :href="item.href"
              class="block border-b border-gray-200 px-4 py-3 font-bold transition-all hover:bg-gray-100"
              @click="isMenuOpen = false"
            >
              {{ item.name }}
            </a>
          </li>
        </ul>
      </nav>
    </transition>
  </header>
</template>

<script setup>
import { ref } from 'vue'
import { Menu, X } from 'lucide-vue-next'

defineProps({
  navItems: {
    type: Array,
    required: true,
  },
})

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}
</script>

<style scoped>
.menu-enter-active,
.menu-leave-active {
  transition:
    max-height 0.3s ease,
    opacity 0.3s ease;
  max-height: 300px;
  overflow: hidden;
}

.menu-enter-from,
.menu-leave-to {
  max-height: 0;
  opacity: 0;
}
</style>
