<script setup>
import groceryItems from '@/components/GroceryItems.vue'
import { groceryItems } from './list'
</script>

<template>
    <div>
        <button class="quantity-add" @click="add(groceryItem)">+</button>
      <h3 class="quantity-count">{{ groceryItem.quantity }}</h3>
      <button class="quantity-subtract" @click="subtract(merch)">-</button>

    </div>
</template>
