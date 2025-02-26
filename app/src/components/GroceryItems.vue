<template>
    <div class="container">
    <div class="card-container">
      <GroceryItemCard
        v-for="(item, index) in shop"
        :key="index"
        :name="item.name"
        :price="item.price"
        :image="item.image"
        :index="item.index"
        v-on:AddtoCart="addingitem"
      />
    </div>
    </div>
</template>

<script setup>
import { ref, computed, onUpdated } from 'vue'
export const groceryItems = ref([
  //export might not be needed
  { name: 'Apple', price: 1.25, img: '/GroceryItems/apple.jpeg', index: 1 },
  { name: 'Orange', price: 1.25, img: '/GroceryItems/orange.jpeg', index: 2 },
  { name: 'Kiwi', price: 2, img: '/GroceryItems/kiwi.jpeg', index: 3 },
  { name: 'Pear', price: 1.25, img: '/GroceryItems/pear.jpeg', index: 4 },
  { name: 'Peach', price: 1.25, img: '/GroceryItems/peach.jpeg', index: 5 },
  { name: 'Banana', price: 1.25, img: '/GroceryItems/banana.jpeg', index: 6 },
  { name: 'Strawberry', price: 3, img: '/GroceryItems/strawberry.jpeg', index: 7 },
  { name: 'Grape', price: 3, img: '/GroceryItems/grape.jpeg', index: 8 },
  { name: 'Blueberry', price: 3, img: '/GroceryItems/blueberry.jpeg', index: 9 },
  { name: 'Mango', price: 2.50, img: '/GroceryItems/mango.jpeg', index: 10 },
  { name: 'Blackberry', price: 3, img: '/GroceryItems/blackberry.jpeg', index: 11 },
  { name: 'Pork', price: 5, img: '/GroceryItems/pork.jpeg', index: 12 },
  { name: 'Chicken', price: 10, img: '/GroceryItems/chicken.jpeg', index: 13 },
  { name: 'Beef', price: 5, img: '/GroceryItems/beef.jpeg', index: 14 },
  { name: 'Steak', price: 6, img: '/GroceryItems/steak.jpeg', index: 15 },
  { name: 'Salmon', price: 10, img: '/GroceryItems/salmon.jpeg', index: 16 },
])
</script>

<style lang="scss" scoped>

</style>
