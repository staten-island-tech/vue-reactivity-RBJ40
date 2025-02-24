<!--appears on the whole website-->
<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/GroceryItems.vue'
import groceryItems from './components/GroceryItems.vue'
</script>

<template>
  <div><RouterView/></div>
  <header>
    <!-- <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" /> -->
    <h1>Grocery shop</h1>
    <p>Buy</p>
    <div v-for="groceryItem in groceryItems" :key="groceryItem">
      <h1>{{ groceryItem.name }}</h1>
      <h2>{{ groceryItem.price }}</h2>
      <img :src="groceryItem.img" />
      <!--might add imgDesc here-->
      <!-- <button @click="$emit"('AddtoCart', index)">Add to Cart</button>
      <slot></slot> -->
    <div class="container">
      <div class="card"><GroceryItems/></div>
    </div>
    </div>

    <div class="wrapper">
      <HelloWorld msg="You did it!" />

      <nav>
        <RouterLink to="/">Products</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
.container{
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  padding: 2rem;
}
.card{
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
}
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
