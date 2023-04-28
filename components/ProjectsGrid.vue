<script lang="ts" setup>
import projects from "@/data/projects"
</script>

<template>
  <div class="container mx-auto">
    <div
      class="grid sm:grid-cols-1 md:grid-cols-2 lg:grid-cols-4 xl:grid-cols-6 gap-8"
    >
      <div v-for="project in projects" :key="project.id" class="bg-gray w-100%">
        <div class="h-32">{{ project.title }}</div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.project-card {
  background-color: gray;
  padding: 8px;

  box-sizing: border-box;
}
</style>
