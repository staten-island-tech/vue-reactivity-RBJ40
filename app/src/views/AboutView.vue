<template>
  <div class="about">
    <h1>Grocery shop</h1>
    <p>Buy</p>
    <h1 v-for="groceryItem in groceryItems">{{ groceryItem.name }}</h1>
    <h2 v-for="groceryItem in groceryItems">{{ groceryItem.price }}</h2>
  </div>
</template>

<script setup>
import groceryItems from './views/list.js'
</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
