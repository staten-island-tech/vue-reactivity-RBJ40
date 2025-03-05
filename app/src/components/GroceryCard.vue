<template>
  <div class="card">
    <h2>{{ name }}</h2>
    <h3>Price: ${{ price }}</h3>
    <img :src="img" alt="Grocery Item"/>
  </div>
</template>

<script setup>
import { groceryItems } from '@/components/GroceryItems.vue';
defineProps({
  msg: {
    name: String,
    price: Number,
    image: String,
    index: Number,
  },
})
</script>

<style scoped>
/* .card{
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  border: 8px solid red;
}
img{
    object-fit: contain;
} */
.card {
  width: 15rem;
  height: 20rem;
  margin: 1rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
  border: 8px solid red;
}

button {
  padding: 5rem;
  display: flex;
}


h3 {
  font-size: 5rem;
}

img {
  height: 25rem;
  border: 5px solid black;
  width: fit-content;
  object-fit: contain;
}
</style>
