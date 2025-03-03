<script setup>
import CharacterCard from '../components/icons/CharacterCard.vue'
import characters from '../assets/BeeMovieCharacters.js'
import ShoppingCartCards from '../components/icons/ShoppingCartCards.vue'
const cart = reactive([])

function addToCart(object, price) {
  cart.push(object) // Figure out what to push
  totalCost.value += price
  console.log(cart)
}
import { ref, reactive } from 'vue'
let totalCost = ref(0)

function clearCart() {
  cart.splice(0, cart.length)
  totalCost.value = 0
}

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
// Step 5: Show the cart (done)
// Step 6: Calculate the cost; use reactive, ref (done)
// Step 7: Remove or clear the cart (by clearing array) (done)
// We want the button on the object to add it to the cart. Cart should be an array; pressing the button should add the button to the array.
</script>

<template>
  <main class="bg-black">
    <div class="header-container w-full flex flex-wrap justify-center object-contain bg-gray-900">
      <h1 class="header font-bold underline text-center text-[64px] text-yellow-400 mb-2">
        Barry B. Benson's small bzzzzzness
      </h1>
    </div>

    <div class="thing-container w-full flex flex-wrap justify-start">
      <div class="card-container w-[70%] flex flex-wrap justify-center p-2">
        <CharacterCard
          v-for="character in characters"
          :key="character.name"
          :character="character"
          @click="addToCart(character, character.price)"
        ></CharacterCard>
      </div>

      <div
        class="cart-container w-[28%] h-fit bg-gray-900 border-2 border-solid border-yellow-400 rounded-2xl p-2 mt-3 flex flex-wrap justify-center align-top"
      >
        <div class="cart-header-container w-full flex flex-wrap justify-center">
          <h2 class="text-[32px] font-medium text-center text-yellow-400">Your Cart</h2>
        </div>
        <div class="cost-header-container w-full flex flex-wrap justify-center">
          <h2 class="text-[32px] font-medium text-center text-yellow-400">
            Cost: ${{ totalCost }}
          </h2>
        </div>
        <div class="button-container w-full flex flex-wrap justify-center">
          <button
            @click="clearCart"
            class="text-[18px] pl-3 pr-3 text-yellow-400 border-solid border-2 border-yellow-400 bg-black rounded-2xl"
          >
            Clear Cart
          </button>
        </div>

        <div class="product-container w-full flex flex-wrap justify-center">
          <ShoppingCartCards
            v-for="character in cart"
            :key="character.name"
            :character="character"
          ></ShoppingCartCards>
        </div>
      </div>
    </div>
  </main>
</template>

<style></style>
