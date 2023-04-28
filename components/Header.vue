<script lang="ts" setup>
import { nextTick, onMounted } from "vue"
const router = useRouter()
const headerHeight = 50 // Replace this value with the height of your sticky header

const scrollToSection = async (sectionId: string) => {
  await router.push("/")
  await nextTick()
  const targetSection = document.getElementById(sectionId)

  if (targetSection) {
    window.scrollTo({
      top: targetSection.offsetTop - headerHeight,
      behavior: "smooth",
    })
  }
}
</script>

<template>
  <div class="w-100% bg-black text-white h-50px sticky top-0">
    <div
      class="flex gap-8 container mx-auto justify-center items-center h-100%"
    >
      <NuxtLink @click.prevent="scrollToSection('hero')">Home</NuxtLink>
      <NuxtLink @click.prevent="scrollToSection('aboutme')">About Me</NuxtLink>
      <NuxtLink @click.prevent="scrollToSection('projects')">Projects</NuxtLink>
      <NuxtLink @click.prevent="scrollToSection('contact')">Contact</NuxtLink>
    </div>
  </div>
</template>
