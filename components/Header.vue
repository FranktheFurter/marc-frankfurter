<script lang="ts" setup>
import { nextTick, onMounted } from "vue";
const router = useRouter();
const headerHeight = 50; // Replace this value with the height of your sticky header

const scrollToSection = async (sectionId: string) => {
  await router.push("/");
  await nextTick();
  const targetSection = document.getElementById(sectionId);

  if (targetSection) {
    window.scrollTo({
      top: targetSection.offsetTop - headerHeight,
      behavior: "smooth",
    });
  }
};
</script>

<template>
  <div class="w-100% bg-black text-white h-50px sticky top-0">
    <div
      class="flex gap-8 container mx-auto justify-center items-center h-100%"
    >
      <NuxtLink class="header-link" @click.prevent="scrollToSection('hero')"
        >Home</NuxtLink
      >
      <NuxtLink class="header-link" @click.prevent="scrollToSection('aboutme')"
        >About Me</NuxtLink
      >
      <NuxtLink class="header-link" @click.prevent="scrollToSection('projects')"
        >Projects</NuxtLink
      >
      <NuxtLink class="header-link" @click.prevent="scrollToSection('contact')"
        >Contact</NuxtLink
      >
    </div>
  </div>
</template>
<style scoped>
.header-link {
  @apply cursor-pointer p-2 border-solid rounded-2 transition-custom ease-in-out duration-150  hover:rounded-1;
}
.transition-custom {
  transition-property: color, background-color, border-color, outline-color,
    text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter,
    backdrop-filter, border-radius;
}
</style>
