<script setup>
import groceryItems from '@/components/GroceryItems.vue'
import { groceryItems } from './list';
</script>

<template>
  <main>
    <h1>Grocery shop</h1>
    <p>Buy</p>
    <div v-for="item in groceryItems" :key="item.name">
      <h2>{{ item.name }} - {{ item.price }}</h2>
      <img :src="item.img" alt="Grocery Item" />
    </div>
  </main>
</template>
