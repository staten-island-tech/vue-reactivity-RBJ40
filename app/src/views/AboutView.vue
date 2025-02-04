<template>
  <div class="about">
    <h1>Grocery shop</h1>
    <p>Buy</p>
    <h1 v-for="groceryItem in groceryItems">{{ groceryItem.name }}</h1>
    <h2 v-for="groceryItem in groceryItems">{{ groceryItem.price }}</h2>
  </div>
</template>

<!-- might need to put this in javascript file. might also add categories for each product
<script>
const groceryItems = [
  { name: 'Apple', price: '$1.25' },
  { name: 'Orange', price: '$1.25' },
  { name: 'Kiwi', price: '$1.25' },
  { name: 'Pear', price: '$1.25'},
  { name: 'Peach', price: '$1.25'},
  { name: 'Banana', price: '$1.25'},
  { name: 'Strawberry', price: '$3'},
  { name: 'Grape', price: '$2'},
  { name: 'Cherry', price: '$3'},
  { name: 'Durian', price: '$1.50'},
  { name: 'Cranberry', price: '$2'},
  { name: 'Blueberry', price: '$3'},
  { name: 'Pork', price: '$5'},
  { name: 'Chicken drumstick', price: '$5'},
  { name: 'Chicken wing', price: '$5'},
  { name: 'Beef', price: '$5'},
  { name: 'Turkey', price: '$5'},
  { name: 'Duck', price: '$5'},
  { name: 'Sausage', price: '$4'}
  { name: 'Fish', price: '$6'}
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
