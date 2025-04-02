<script setup lang="ts">
import type { PropType } from "vue";

defineProps({
  title: {
    type: String,
    required: true,
  },
  date: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
  link: {
    type: Object as PropType<{ name: string; href: string }>,
  },
});
</script>

<template>
  <h3 class="font-gochi text-xl text-zinc-800">{{ title }}</h3>
  <span class="text-zinc-700">{{ date }}</span>
  <p class="text-zinc-700">{{ description }}</p>
  <a :href="link.href" class="text-sky-700" v-if="link">{{ link.name }}</a>
</template>
