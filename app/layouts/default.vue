<template>
  <div class="flex flex-col min-h-screen bg-slate-900 text-gray-100">
    <!-- Header / Navbar -->
    <Header />

    <!-- Page Content -->
    <NuxtPage class="flex-grow" />

    <!-- Footer -->
    <Footer />
  </div>
</template>

<script setup>
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer.vue'

</script>
