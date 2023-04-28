<script lang="ts" setup>
import projects from "@/data/projects"
</script>

<template id="projects">
  <section id="projects" class="container mx-auto py-8">
    <div
      class="grid sm:grid-cols-1 md:grid-cols-2 lg:grid-cols-4 xl:grid-cols-5 gap-8"
    >
      <div v-for="project in projects" :key="project.id" class="bg-gray w-100%">
        <NuxtLink :to="`projects/${project.id}`">
          <div class="h-300px">{{ project.title }}</div>
        </NuxtLink>
      </div>
    </div>
  </section>
</template>

<style scoped>
.project-card {
  background-color: gray;
  padding: 8px;

  box-sizing: border-box;
}
</style>
