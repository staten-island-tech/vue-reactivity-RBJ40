<script setup>
export const groceryItems = [
  { name: 'Apple', price: '$1.25', img: '/GroceryItems/apple.jpeg' },
  { name: 'Orange', price: '$1.25', img: '/GroceryItems/orange.jpeg' },
  { name: 'Kiwi', price: '$2', img: '/GroceryItems/kiwi.jpeg' },
  { name: 'Pear', price: '$1.25', img: '/GroceryItems/pear.jpeg' },
  { name: 'Peach', price: '$1.25', img: '/GroceryItems/peach.jpeg' },
  { name: 'Banana', price: '$1.25', img: '/GroceryItems/banana.jpeg' },
  { name: 'Strawberry', price: '$3', img: '/GroceryItems/strawberry.jpeg' },
  { name: 'Grape', price: '$3', img: '/GroceryItems/grape.jpeg' },
  { name: 'Blueberry', price: '$3', img: '/GroceryItems/blueberry.jpeg' },
  { name: 'Mango', price: '$2.50', img: '/GroceryItems/mango.jpeg' },
  { name: 'Blackberry', price: '$3', img: '/GroceryItems/blackberry.jpeg' },
  { name: 'Pork', price: '$5', img: '/GroceryItems/pork.jpeg' },
  { name: 'Chicken', price: '$10', img: '/GroceryItems/chicken.jpeg' },
  { name: 'Beef', price: '$5', img: '/GroceryItems/beef.jpeg' },
  { name: 'Steak', price: '$6', img: '/GroceryItems/steak.jpeg' },
  { name: 'Salmon', price: '$10', img: '/GroceryItems/salmon.jpeg' },
];
defineProps({
  msg: {
    name: String,
    price: Number,
    image: String,
  },
})
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h3>
      You’ve successfully created a project with
      <a href="https://vite.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>.
    </h3>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
