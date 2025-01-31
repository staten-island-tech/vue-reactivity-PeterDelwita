<template>
  <div>
    <h2>{{ character.name }}</h2>
    <h3>{{ character.role }}</h3>
    <h3>{{ character.price }}</h3>
  </div>
</template>

<script setup>
defineProps({
  character: Object,
})
// Images go in public folder
// Put character cards in container
// Use Tailwind for this project
</script>

<style scoped></style>
