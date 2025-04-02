<script setup lang="ts">
import type { PropType } from "vue";

defineProps({
  review: {
    type: Object as PropType<{ name: string; job: string; review: string }>,
    required: true,
  },
});
</script>

<template>
  <article class="flex flex-col gap-1 border-2 border-zinc-700 rounded-2xl p-3">
    <p>{{ review.review }}</p>
    <div class="flex flex-col">
      <span class="text-zinc-700 text-sm">{{ review.name }}</span>
      <span class="text-zinc-700 text-sm">{{ review.job }}</span>
    </div>
  </article>
</template>
