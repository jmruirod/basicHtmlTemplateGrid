<script setup lang="ts">
import type { PropType } from "vue";
import SectionElement from "./SectionElement.vue";

defineProps({
  title: {
    type: String,
    required: true,
  },
  items: {
    type: Array as PropType<{ title: string; date: string; description: string; link?: { name: string; href: string } }[]>,
    required: true,
  },
});
</script>

<template>
  <section class="w-full xl:w-auto py-8 sm:py-4 flex flex-col gap-2">
    <h2 class="font-gochi text-3xl text-zinc-800 px-6 text-center xl:text-left">{{ title }}</h2>
    <ul class="divide-y-1 divide-zinc-700 flex flex-col gap-4 [&>li]:px-6">
      <li v-for="(item, index) in items" :key="'item' + index">
        <SectionElement :title="item.title" :date="item.date" :description="item.description" :link="item.link" />
      </li>
    </ul>
  </section>
</template>
