<template>
  <div class="card w-[90%] flex flex-wrap justify-start align-top mb-3">
    <h3 class="text-[12px] text-yellow-400">Name: {{ item.name }}</h3>
    <h3 class="text-[12px] text-yellow-400">Price: {{ item.price }}</h3>
  </div>
</template>

<script setup>
import { ref, reactive } from 'vue' // Add separate component for items added to cart; show cart also
import { item } from '../components/icons/CharacterCard.vue'
const props = defineProps({
  item: Object,
})
</script>

<style scoped></style>
