<script setup>
import GroceryItems from '@/components/GroceryItems.vue';
import { ref } from 'vue'
const price = ref('$0.00'); //starting price = $0.00

function deleteItem = (index) => {
  console.log(index, 'Delete item')
  cart.splice(index, 1);
}
deleteItem();
  
function addItem = (index) => {
  console.log(index, 'Add Item')
  cart.push({ name: item.name, price: item.price }) 
}
addItem();
  
defineProps({
  cart: Array, 
})
</script>

<template>
  <div class="cart">
    <h2>Shopping Cart:</h2>
    <ul>
      <li v-for="(item, index) in cart" :key="index">
        <h2>{{ item.name }} - ${{ item.price }}</h2>
        <button @click="deleteItem(index)">Remove Item</button>
        <button @click="addItem(index)">Add to Cart</button>
      </li>
    </ul>
    <h3>Total Cost: ${{ totalPrice.toFixed(2) }}</h3>   <!--makes totalPrice have two decimal places-->
  </div>
</template>


<style scoped>
.cart {
  height: fit-content;
  width: 25%;
  border: 5px solid black;
}

</style>
