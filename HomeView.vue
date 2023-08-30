<script setup>
// import CartBIN from '../components/CartBIN.vue'


</script>

<template>
  <main>
    <br>
    <div class="slideshow-container">
      <div class="mySlides fade">
        <img src="https://www.miss-sophie.com/cdn/shop/articles/DE-Springblossom-Website-Magazin-20220211-3840x2160_0.5-v3.png?v=1645810652" style="width:100%">
      </div>
    </div>

    <div>
      <hr class="line1">
    </div>
    
    <div class="row">
      <div class="column">
        <img src="https://images.squarespace-cdn.com/content/v1/58a4b2d43a04112a74b427fe/1656461296638-DDEZQYCKROJXNDUYI5GW/Quinn12.jpg?format=1000w" alt="Dress1" style="width:75%">
        <br>
        <!-- <button class="button">Add to Cart</button> -->
        <hr class="line2">
      </div>
      <div class="column">
        <img src="https://luvbridal.com.au/wp-content/uploads/2023/07/OZEN-D3-600x800.jpg" alt="Dress2" style="width:75%">
        <!-- <button class="button">Add to Cart</button> -->
        <hr class="line2">
      </div>
      <div class="column">
        <img src="https://ajeworld.com.au/cdn/shop/products/22RE5588_IVRY_1.jpg?v=1669644126" alt="Dress3" style="width:75%">
        <!-- <button class="button">Add to Cart</button> -->
        <hr class="line2">
      </div>
    </div> 
    <TheWelcome />
  </main>
</template>

<style scoped>

button{
  margin-buttom: 20px;
}

.line1 {
  width: 70%;
  text-align: center;
  margin-top: 30px;
  margin-bottom: 30px;
}

.line2 {
  width: 40%;
  text-align: center;
  margin-top: 30px;
}

.column{
  width: 30%;
  display: block;
  margin-left: auto;
  margin-right: auto;
  margin-top: 30px;
}

.button{
  display: block;
  width: 50%;
  border: none;
  background-color: #59788E;
  color: white;
  padding: 14px 28px;
  cursor: pointer;
  text-align: center;
}

.button:hover{
  background-color: lightgrey;
  color: black;
}

@media only screen and (max-width: 300px) {
  .text {font-size: 11px}
}

@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}

.active {
  background-color: #717171;
}

/* Fading animation */
.fade {
  animation-name: fade;
  animation-duration: 1.5s;
}

@keyframes fade {
  from {opacity: .4} 
  to {opacity: 1}
}

* {box-sizing: border-box;}
body {font-family: Verdana, sans-serif;}

/* Picture Container */
.slideshow-container {
  max-width: 1000px;
  position: relative;
  margin-left: auto;
  margin-right: auto;
}

/* Caption text */
.text {
  color: #f2f2f2;
  font-size: 15px;
  padding: 8px 12px;
  position: absolute;
  bottom: 8px;
  width: 100%;
  text-align: center;
}

</style>
