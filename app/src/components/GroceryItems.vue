<template>
    <div class="container">
    <div class="card-container">
      <GroceryCard
        v-for="(item, index) in groceryItems"
        :key="index"
        :name="item.name"
        :price="item.price"
        :image="item.image"
        v-on:AddtoCart="addingitem"
      />  <!--chatgpt-->
    </div>
    <div class="cart">
      <h2>Shopping Cart:</h2>
      <p v-for="(item, index) in cart" :key="index">
        <h2> {{ item.name }} - ${{ item.price }} </h2>
        <button @click="deleteItem(index)">Remove Item</button>
      </p>
      <h3>Total Cost: ${{ totalPrice.toFixed(2) }}</h3>   <!--makes totalPrice have two decimal places-->
    </div>
    </div>
</template>

<script setup>
import { ref, computed, onUpdated } from 'vue'
const groceryItems = ref([
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

const cart = ref([])

function addItem(index) {  //index because it's unique
  console.log(index, 'Adding item to cart')
  const item = shop.value[index] 
  if (item) {
    cart.push({ name: item.name, price: item.price }) 
  }
}
addItem();

function deleteItem(index) {
  cart.splice(index, 1);
}
deleteItem();
  
const totalPrice = computed(() => {
  return cart.reduce((sum, item) => sum + item.price, 0);
})

  
onUpdated(() => {
  console.log('Cart updated:', cart.value)
})
</script>

<style lang="css" scoped>
.card-container {
  width: 70%;
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  width: 100rem;
}
.cart {
  height: fit-content;
  width: 40%;
  background-color: gray;
}

.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.cards {
  display: flex;
  flex-wrap: wrap;
  width: 50%;
}
h2{
  font-size: 5rem;
}
</style>
