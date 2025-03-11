<script setup>
import GroceryItems from '@/components/GroceryItems.vue';
//import {{ groceryItems }} from '@/components/GroceryItems.vue';
</script>

<template>
  <main>
    <h1>Grocery shop</h1>
    <p>Buy</p>
    <div v-for="item in groceryItems" :key="item.name">
      <h2>{{ item.name }} - {{ item.price }}e</h2>
      <img :src="item.img" alt="Grocery Item" />
    </div>
  </main>
</template>

<style scoped>
h1, p {
  font-size: 2rem;
  align-content: center;
}

</style>
