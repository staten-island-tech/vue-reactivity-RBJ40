<script setup>
import ShoppingCart from '@/components/ShoppingCart.vue';
import GroceryItems from '@/components/GroceryItems.vue';
</script>

<template>
  <div class="cards"><GroceryItems /></div>
</template>

<style lang="css" scoped>
.cards{
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
}
</style>
