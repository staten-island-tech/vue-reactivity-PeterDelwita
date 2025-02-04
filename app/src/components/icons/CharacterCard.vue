<template>
  <div
    class="card w-[30%] flex flex-wrap border-solid border-2 rounded-2xl border-black bg-yellow-400 justify-center"
  >
    <!--Fix the cards here...-->
    <div class="text-center">
      <h2 class="text-[16px]">{{ character.name }}</h2>
      <h3>{{ character.role }}</h3>
      <h3>{{ character.price }}</h3>
    </div>
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
