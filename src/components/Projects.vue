<script setup>
import projects from "@/data/projects";
import { Carousel, Slide } from 'vue-carousel';
</script>

<template>
  <section id="projects" class="flex flex-col items-center py-16">
    <h2 class="mt-5 mb-28 text-4xl font-bold text-black">Projects</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10 m-4">
      <div v-for="(project, i) of projects" :key="project.title" class="grid place-items-center text-center gap-5 p-8 bg-white bg-base-100 shadow-xl rounded-lg" :class="i == 1 ? 'lg:-translate-y-10' : ''">
        <div>
          <img :src="project.image" alt="" class="w-full h-auto">
        </div>
        <h3 class="text-black text-2xl font-bold">{{ project.title }}</h3>
        <p class="text-black w-[90%]">{{ project.desc }}</p>
        <a :href="project.github" target="_blank" rel="noopener noreferrer" class="border border-black p-2 rounded-3xl flex">
            <img src="@/assets/img/25231.png" alt="GitHub" class="w-5 h-5">
            <span class="ml-2">GitHub</span>
        </a>
      </div>
    </div>
  </section>
</template>
