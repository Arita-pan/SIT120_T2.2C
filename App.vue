<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { ref } from 'vue'


</script>

<template>

  <header>
    
    <div>
      <nav>
        <ul>
          <li class="logo">Luminar</li>
          <li><RouterLink to="/">Home</RouterLink></li>
          <li><RouterLink to="/newcollection">New Collection</RouterLink></li>
          <!-- <li><RouterLink to="/sale">Sale</RouterLink></li> -->
          <!-- <li><RouterLink to="/cart">Cart</RouterLink></li> -->
        </ul>
      </nav>
    </div>
  </header>

  <RouterView/>
</template>

<style scoped>

.logo{
  font-family: Bradley Hand, cursive;
  color: azure;
  text-align: center;
  display: block;
  padding: 20px 25px;
}

nav {
  font-family: Monospace, serif;
}

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333;
}

li {
  float: left;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 20px 25px;
  text-decoration: none;
}

li a:hover {
  background-color: #111;
}



</style>
