<template>
  <header class="bg-gray-800 shadow-lg sticky top-0 z-50">
    <nav class="container mx-auto px-6 py-4">
      <div class="flex items-center justify-between">
        <NuxtLink to="/" class="text-2xl font-bold text-blue-400 hover:text-blue-300">
          Portfolio
        </NuxtLink>

        <!-- Desktop Menu -->
        <div class="hidden md:flex space-x-8">
          <NuxtLink v-for="link in navLinks" :key="link.path" :to="link.path"
            class="text-gray-300 hover:text-blue-400 transition-colors duration-200" active-class="text-blue-400">
            {{ link.name }}
          </NuxtLink>
        </div>

        <!-- Mobile Menu Button -->
        <button @click="mobileMenuOpen = !mobileMenuOpen" class="md:hidden text-gray-300 hover:text-blue-400">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path v-if="!mobileMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16" />
            <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
      </div>

      <!-- Mobile Menu -->
      <div v-if="mobileMenuOpen" class="md:hidden mt-4 space-y-2">
        <NuxtLink v-for="link in navLinks" :key="link.path" :to="link.path" @click="mobileMenuOpen = false"
          class="block text-gray-300 hover:text-blue-400 py-2 transition-colors duration-200"
          active-class="text-blue-400">
          {{ link.name }}
        </NuxtLink>
      </div>
    </nav>
  </header>
</template>

<script lang="ts" setup>
const mobileMenuOpen = ref(false)

const navLinks = [
  // { name: 'Home', path: '/' },
  { name: 'About', path: '/about' },
  { name: 'Skills', path: '/skills' },
  { name: 'Contact', path: '/contact' }
]
</script>

<style></style>