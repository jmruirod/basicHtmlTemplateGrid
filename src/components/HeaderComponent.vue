<script setup lang="ts">
import type { PropType } from "vue";

defineProps({
  logo: {
    type: String,
    required: true,
  },
  name: {
    type: String,
    required: true,
  },
  title: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
  links: {
    type: Array as PropType<{ name: string; href: string }[]>,
    required: true,
  },
});
</script>
<template>
  <header
    class="grid xl:auto-cols-max xl:justify-between justify-items-center xl:justify-items-normal xl:grid-rows-[1fr_auto] xl:auto-rows-min gap-4 py-8 px-4 sm:p-4"
  >
    <div class="flex flex-col xl:flex-row items-center gap-2 xl:gap-4">
      <a class="font-gochi px-4 py-2 inline-block rounded-xl bg-zinc-800 text-white text-4xl text-center">{{ logo }}</a>
      <h1 class="text-2xl font-bold text-zinc-800">{{ name }}</h1>
    </div>

    <ul class="flex items-center gap-2 text-xl text-zinc-800">
      <li v-for="(link, index) in links" :key="link.href">
        <a :href="link.href">{{ link.name }}</a>
        <span v-if="index !== links.length - 1"> /</span>
      </li>
    </ul>

    <div class="xl:col-span-2 min-h-[130px] xl:min-h-[200px] flex flex-col justify-center items-center">
      <h1 class="font-gochi text-6xl text-zinc-800 text-center lg:text-left">{{ title }}</h1>
      <span class="text-xl text-zinc-700">{{ description }}</span>
    </div>
  </header>
</template>
