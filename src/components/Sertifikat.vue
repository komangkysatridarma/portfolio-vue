<script setup>
import sertifikats from "@/data/sertifikat";
</script>

<template>
    <section id="sertifikat" class="flex flex-col items-center py-16 mb-16">
      <h2 class="mt-5 mb-16 text-4xl font-bold text-black">Sertifikat</h2>
      <div class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-4 gap-10 m-4">
            <div v-for="serti of sertifikats" class="max-w-sm p-7 bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700">
                <div>
                    <img :src="serti.image" class="w-full h-auto">
                </div>
                <h3 class="text-black text-xl font-bold mt-2">{{ serti.title }}</h3>
            </div>
      </div>
    </section>
  </template>
  