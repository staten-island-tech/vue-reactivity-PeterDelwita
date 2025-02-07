<script setup>
import CharacterCard from '../components/icons/CharacterCard.vue'
import characters from '../assets/BeeMovieCharacters.js'
import cart from '../components/icons/CharacterCard.vue'
import { ref, reactive } from 'vue'

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
// Step 2: Show Characters on Screen (worry about images later) (done)
// Step 2.5: Fix cards (done)
// Step 3: "Cart" Array (done)
// Step 4: Add to cart (done)
// Step 5: Show the cart
// Step 6: Calculate the cost; use reactive
// Step 7: Remove or clear the cart (by clearing array)
// We want the button on the object to add it to the cart. Cart should be an array; pressing the button should add the button to the array.
</script>

<template>
  <main class="bg-black">
    <div class="header-container w-full flex flex-wrap justify-center object-contain bg-gray-900">
      <h1 class="header font-bold underline text-center text-[64px] text-yellow-400 mb-2">
        Barry B. Benson's small bzzzzzness
      </h1>
    </div>

    <!--Bee Movie dating app!!!-->
    <!--What do I want to be my components?-->
    <!--Cards of Bee Movie characters should be a component (a dating app?) along with a heading introducing the site and cards for the shopping cart. (Shopping cart should also be a component?)-->
    <!--File will be big -->
    <div class="thing-container w-full flex flex-wrap justify-start">
      <!--Doesn't cover whole screen for whatever reason-->
      <div class="card-container w-[70%] flex flex-wrap justify-center p-2">
        <CharacterCard
          v-for="character in characters"
          :key="character.name"
          :character="character"
        ></CharacterCard>
      </div>
      <div class="cart-container w-[30%] h-dvh bg-gray-900 flex flex-wrap justify-center align-top">
        <!-- Supposed to show the cart-->
        <h2 class="text-[32px] font-medium text-center text-yellow-400">Your Cart</h2>
        <!--Why don't I try reusing CharacterCard in the cart?? See what happens (need to figure out costs)-->
        <ShoppingCartCards v-for="item in cart" :key="item.name" :item="item"></ShoppingCartCards>
      </div>
    </div>
  </main>
</template>

<style></style>
