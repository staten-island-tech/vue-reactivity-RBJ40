<script setup>
import { groceryItems } from './components/GroceryItems.vue'
</script>

<template>
  <main>
    <h1>Grocery shop</h1>
    <p>Buy</p>
    <div v-for="groceryItem in groceryItems" :key="groceryItem">
      <h1>{{ groceryItem.name }}</h1>
      <h2>{{ groceryItem.price }}</h2>
      <img :src="groceryItem.img" />
      <!--might add imgDesc here-->
      <!-- <button @click="$emit"('AddtoCart', index)">Add to Cart</button>
      <slot></slot> -->
    <div class="container">
      <div class="card"><GroceryItems/></div>
    </div>
    </div>
  </main>
</template>
