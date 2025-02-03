<script setup>
import CharacterCard from '../components/icons/CharacterCard.vue'
import characters from '../BeeMovieCharacters.js'
</script>

<template>
  <main>
    <h1 class="text-3xl font-bold underline text-center">Big Bzzzzness, by Barry B. Benson</h1>
    <!--Bee Movie dating app!!!-->
    <!--What do I want to be my components?-->
    <!--Cards of Bee Movie characters should be a component (products to sell, or a dating app?) along with a heading introducing the site and cards for the shopping cart. (Shopping cart should also be a component?)-->
    <!--File will be big -->
    <div class="container w-full flex flex-wrap">
      <CharacterCard
        v-for="character in characters"
        :key="character.name"
        :character="character"
      ></CharacterCard>
    </div>
  </main>
</template>

<style></style>
