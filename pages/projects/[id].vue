<script lang="ts" setup>
const router = useRoute()
const routeId = router.params.id
</script>

<template>
  <div>Projects by id: {{ routeId }}</div>
</template>

<style scoped></style>
