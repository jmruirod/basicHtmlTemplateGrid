<script setup lang="ts">
import FooterComponent from "./components/FooterComponent.vue";
import MainContentSection from "./components/MainContentSection.vue";
import HeaderComponent from "./components/HeaderComponent.vue";
import AsideContentSection from "./components/AsideContentSection.vue";

const links = [
  { name: "Inicio", href: "#" },
  { name: "Proyectos", href: "#" },
  { name: "Articulos", href: "#" },
  { name: "Contacto", href: "#" },
];

const projectsItems = [
  { name: "Portafolio HTML", href: "#" },
  { name: "Calculadora", href: "#" },
  { name: "App Quiz", href: "#" },
  { name: "Contador", href: "#" },
  { name: "Pagina de producto", href: "#" },
];

const experienceItems = [
  {
    title: "Desarrollador Full Stack",
    date: "2023 - 2024",
    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
    link: { name: "Ver mas", href: "#" },
  },
  {
    title: "Desarrollador Web",
    date: "2020 - 2021",
    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
    link: { name: "Ver mas", href: "#" },
  },
];

const educationItems = [
  {
    title: "Desarrollo de Aplicaciones Multiplataforma",
    date: "2021 - 2023",
    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
  },
  {
    title: "Bachillerato científico-tecnológico",
    date: "2020 - 2021",
    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
  },
];

const reviews = [
  { name: "Juan Perez", job: "Desarrollador Web", review: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos." },
  { name: "Juan Perez", job: "Desarrollador Web", review: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos." },
  { name: "Juan Perez", job: "Desarrollador Web", review: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos." },
  { name: "Juan Perez", job: "Desarrollador Web", review: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos." },
  { name: "Juan Perez", job: "Desarrollador Web", review: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos." },
  { name: "Juan Perez", job: "Desarrollador Web", review: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos." },
];
</script>

<template>
  <div class="h-full w-full md:w-[65%] md:mx-auto bg-white rounded-xl md:border-3 border-zinc-700 shadow-2xl">
    <HeaderComponent
      logo="R"
      name="José Manuel Ruiz Rodriguez"
      title="Full Stack Developer"
      description="Vue con Tailwind para el layout."
      :links="links"
      class="border-b-3 border-zinc-700"
    />
    <main class="min-h-[500px] grid grid-cols-1 md:grid-cols-2 xl:grid-cols-[230px_1fr_1fr] border-b-3 border-zinc-700">
      <AsideContentSection
        title="Proyectos"
        :items="projectsItems"
        class="md:col-span-2 xl:col-span-1 text-center xl:text-left border-b-3 xl:border-b-0 xl:border-r-3 border-zinc-700"
      />
      <MainContentSection title="Experiencia Laboral" :items="experienceItems" class="md:border-r-3 border-b-3 md:border-b-0 border-zinc-700" />
      <MainContentSection title="Educación" :items="educationItems" />
    </main>
    <FooterComponent title="Reviews de mis profesores" :reviews="reviews" />
  </div>
</template>

<style scoped></style>
