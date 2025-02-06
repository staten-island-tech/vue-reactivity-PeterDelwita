<template>
  <div
    class="card w-[30%] flex border-solid border-2 rounded-2xl border-yellow-400 bg-black justify-center items-center m-2 p-2"
  >
    <!--Fix the cards here...-->
    <div class="text-center">
      <h2 id="name" class="text-[24px] text-yellow-400">{{ character.name }}</h2>
      <h3 id="role" class="text-[20px] text-yellow-400">{{ character.role }}</h3>
      <h3 id="price" class="text-[20px] text-yellow-400">{{ character.price }}</h3>
      <button
        @click="addToCart"
        class="text-[18px] text-yellow-400 border-solid border-2 border-yellow-400 bg-black rounded-2xl"
      >
        Date!!
      </button>
    </div>
  </div>
</template>

<script setup>
import { ref, reactive } from 'vue'
const props = defineProps({
  character: Object,
})

const cart = reactive([])
function addToCart() {
  cart.push({
    name: props.character.name,
    price: props.character.price,
  })
  console.log(cart)
}

// Images go in public folder
// Put character cards in container
// Use Tailwind for this project
</script>

<style scoped></style>
