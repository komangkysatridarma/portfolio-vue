<script setup>
import { ref } from 'vue';

const isMobileMenuOpen = ref(false);

function toggleMobileMenu() {
  isMobileMenuOpen.value = !isMobileMenuOpen.value;
}
</script>

<template>
  <section id="home">
    <nav class="flex items-center justify-between container pt-10">
      <div class="flex">
        <h1 class="text-black lg:text-2xl font-bold sm:text-xs">Portfolio Website</h1>
      </div>
      <div class="flex items-center gap-4 md:gap-10">
        <!-- Tambahkan ikon hamburger dan event handler -->
        <button @click="toggleMobileMenu" class="lg:hidden text-black">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
          </svg>
        </button>
        <!-- Tampilkan tautan navigasi di desktop -->
        <div class="hidden lg:flex items-center gap-4 md:gap-10">
          <a class="text-black font-medium" href="#home">Home</a>
          <a class="text-black font-medium" href="#about">About</a>
          <a class="text-black font-medium" href="#projects">Projects</a>
          <a class="text-black font-medium" href="#sertifikat">Sertifikat</a>
        </div>
      </div>
    </nav>

    <!-- Tampilkan menu seluler jika diaktifkan -->
    <div class="lg:hidden flex justify-end items-end">
    <div v-if="isMobileMenuOpen" class="lg:hidden z-10 bg-white divide-y divide-gray-100 rounded-lg shadow w-44 dark:bg-gray-700">
      <!-- Tambahkan tautan navigasi di sini -->
      <a class="text-black font-medium block mb-1" href="#home">Home</a>
      <a class="text-black font-medium block mb-1" href="#about">About</a>
      <a class="text-black font-medium block mb-1" href="#projects">Projects</a>
      <a class="text-black font-medium block mb-1" href="#sertifikat">Sertifikat</a>
    </div>
  </div>
  </section>
</template>

<!-- Import Font Awesome styles -->
<style>
@import "@/../node_modules/@fortawesome/fontawesome-free/css/all.css";
</style>
