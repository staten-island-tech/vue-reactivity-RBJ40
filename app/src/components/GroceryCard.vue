<template>
  <div class="card">
    <h2>{{ name }}</h2>
    <h3>Price: ${{ price }}</h3>
    <img :src="img" alt="Grocery Item"/>
    <button @click="$emit('AddtoCart', index)">Add to Cart</button>
  </div>
</template>

<script setup>
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
.card{
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  border: 8px solid red;
  width: 15rem;
  height: 20rem;
}
button {
  padding: 5rem;
}

img {
  height: 25rem;
  width: fit-content;
  object-fit: contain;
}
</style>
