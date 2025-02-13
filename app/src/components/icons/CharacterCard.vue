<template>
  <div
    class="card w-[30%] max-[600px]:w-[70%] flex border-solid border-2 rounded-2xl border-yellow-400 bg-black justify-center items-center m-2 p-2"
  >
    <div class="text-center">
      <h2 id="name" class="text-[20px] font-bold text-yellow-400">{{ character.name }}</h2>
      <h3 id="role" class="text-[18px] text-yellow-400">{{ character.role }}</h3>
      <h3 id="price" class="text-[20px] text-yellow-400">${{ character.price }}</h3>
      <button
        @click="addToCart"
        class="text-[18px] text-yellow-400 pl-3 pr-3 border-solid border-2 border-yellow-400 bg-black rounded-2xl"
      >
        Buy
      </button>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  character: Object,
})

// Images go in public folder
// Put character cards in container
// Use Tailwind for this project
</script>

<style scoped></style>
