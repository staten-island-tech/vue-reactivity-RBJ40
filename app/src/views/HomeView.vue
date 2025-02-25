<script setup>
import groceryItems from '@/components/GroceryItems.vue'
import { groceryItems } from './list';
import ShoppingCart from '@/components/ShoppingCart.vue';
</script>

<template>
  <main>
    <div><ShoppingCart/></div>
    <h1>Grocery shop</h1>
    <p>Buy</p>
    <div v-for="item in groceryItems" :key="item.name">
      <h2>{{ item.name }} - {{ item.price }}</h2>
      <img :src="item.img" alt="Grocery Item" />
    </div>
    <div class="cart"><ShoppingCart/></div>
  </main>
</template>
<style lang="css" scoped>
.card{
  display: flex;
  flex-wrap: wrap;
}
</style>
