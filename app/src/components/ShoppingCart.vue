<script setup>
import { ref } from 'vue'
const price = ref('$0.00'); //starting price = $0.00

function deleteItem = (index) => {
  console.log(index, 'Delete item')
  item.splice(index, 1);
}
deleteItem();
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
      </li>
    </ul>
    <h3>Total Cost: ${{ price }}</h3>
  </div>
</template>


<style scoped>
.cart {
  height: fit-content;
  width: 25%;
  border: 5px solid black;
}

</style>
