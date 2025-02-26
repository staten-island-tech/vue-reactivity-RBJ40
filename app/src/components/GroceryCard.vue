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

<style lang="css" scoped>
.card{
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  border: 8px solid red;
}
img{
    object-fit: contain;
}
</style>
