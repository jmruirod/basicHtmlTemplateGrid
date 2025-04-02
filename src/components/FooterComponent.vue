<script setup lang="ts">
import type { PropType } from "vue";
import ReviewCard from "./ReviewCard.vue";

defineProps({
  title: {
    type: String,
    required: true,
  },
  reviews: {
    type: Array as PropType<{ name: string; job: string; review: string }[]>,
  },
});
</script>

<template>
  <footer class="min-h-[200px] py-8 px-6 flex flex-col">
    <h2 class="font-gochi text-3xl text-zinc-800 text-center xl:text-left">{{ title }}</h2>
    <section class="grid grid-cols-[repeat(auto-fit,minmax(250px,1fr))] gap-4 py-2 lg:px-2">
      <ReviewCard v-for="(review, index) in reviews" :key="'item' + index" :review="review" />
    </section>
    <section class="min-h-[100px] flex justify-center items-end">
      <h2 class="font-gochi text-3xl text-zinc-800">© Todos los derechos reservados</h2>
    </section>
  </footer>
</template>
