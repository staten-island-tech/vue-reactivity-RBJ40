<template>
  <div class="about">
    <h1>Grocery shop</h1>
    <p>Buy</p>
    <div v-for="groceryItem in groceryItems" :key="groceryItem">
      <h1>{{ groceryItem.name }}</h1>
      <h2>{{ groceryItem.price }}</h2>
      <img :src="groceryItem.img" />
      <!--might add imgDesc here-->
      <slot></slot>
    </div>
  </div>
</template>

<script setup>
import groceryItems from '../views/list.js' //possibly imported wrong???
</script>

<style scoped>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
