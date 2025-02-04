<script setup>
import CharacterCard from '../components/icons/CharacterCard.vue'
import characters from '../assets/BeeMovieCharacters.js'

// Example 1:
// ItemsArr
// Put items on Screen
// Add to Cart
// Cart Array
// Calc Cost
// Remove/reset cart
// Show the cart (same as step 2)

// Example 2:
// ItemArr (w/ types)
// Buttons for Filtering
// Display filtered weapons
// Add to Weapon (Arr)
// Display Add-Ons

// Example 3:
// Create Tiers (data type - object)
// Name: S Tier, Items: []
// Show tiers
// Create items to be tiered (ex. fruit)
// fruit array, show fruit
// Add to Tier button (do a dropdown, we are not at the level of drag-and-drop
//

// My Project
// Step 1: Character Array (done!)
// Step 2: Show Characters on Screen (worry about images later)
// Step 2.5: Fix cards
// Step 3: "Cart" Array
// Step 4: Add to cart
// Step 5: Show the cart
// Step 6: Calculate the cost; use reactive
// Step 7: Remove or clear the cart
</script>

<template>
  <main>
    <h1 class="text-3xl font-bold underline text-center">Big Bzzzzness, by Barry B. Benson</h1>
    <!--Bee Movie dating app!!!-->
    <!--What do I want to be my components?-->
    <!--Cards of Bee Movie characters should be a component (a dating app?) along with a heading introducing the site and cards for the shopping cart. (Shopping cart should also be a component?)-->
    <!--File will be big -->
    <div class="container w-full flex flex-wrap justify-center">
      <CharacterCard
        v-for="character in characters"
        :key="character.name"
        :character="character"
      ></CharacterCard>
    </div>
  </main>
</template>

<style></style>
