<template>
  <div class="about">
    <h1>Grocery shop</h1>
    <p>Buy</p>
    <h1 v-for="groceryItem in groceryItems">{{ groceryItem.name }}</h1>
    <h2 v-for="groceryItem in groceryItems">{{ groceryItem.price }}</h2>
  </div>
</template>

<!-- might need to put this in javascript file
<script>
const groceryItems = [
  { name: 'Apple', price: '$1.25' },
  { name: 'Orange', price: '$1.25' },
  { name: 'Kiwi', price: '$5' },
  { name: 'Pear', price: '$1.25'},
  { name: 'Peach', price: '$1.25'},
]
</script> -->

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
