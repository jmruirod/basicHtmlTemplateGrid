<script setup lang="ts">
import type { PropType } from "vue";

defineProps({
  title: {
    type: String,
    required: true,
  },
  items: {
    type: Array as PropType<{ name: string; href: string }[]>,
    required: true,
  },
});
</script>

<template>
  <section class="w-full xl:w-auto xl:py-4 flex flex-col xl:gap-2">
    <h2 class="font-gochi text-3xl text-zinc-800 py-2 xl:py-0 xl:px-6">{{ title }}</h2>
    <ul
      class="border-t-2 border-zinc-700 xl:border-y-0 divide-y-1 divide-zinc-700 [&>li>a]:block xl:[&>li>a]:inline [&>li>a]:w-full [&>li>a]:py-1.5 xl:[&>li>a]:py-0 xl:[&>li>a]:px-6 [&>li>a]:hover:bg-zinc-200 xl:[&>li>a]:hover:bg-inherit [&>li>a]:transition-colors [&>li>a]:duration-300"
    >
      <li v-for="item in items" :key="item.href">
        <a :href="item.href">{{ item.name }}</a>
      </li>
    </ul>
  </section>
</template>
