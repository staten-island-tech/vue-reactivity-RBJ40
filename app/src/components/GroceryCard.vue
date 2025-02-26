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
  font-size: 1.6rem;
}


h3 {
  font-size: 2rem;
  color: rgb(13, 107, 101);
}

img {
  height: 25rem;
  width: fit-content;
  object-fit: contain;
  margin: 0.3rem;
}
</style>
