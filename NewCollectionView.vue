<script>
export default {
  name: "App",
  data: () => {
    return {
      page:'products',
      cart: [],
      products: [
        {
          name: "T-Shirt",
          cost: "$30",
          image: "https://www.mrporter.com/variants/images/43769801097337434/in/w2000_q60.jpg",
        },
        {
          name: "Polo Shirt",
          cost: "$50",
          image: "https://www.careofcarl.no/bilder/artiklar/zoom/14316211r_1.jpg?m=1666701532",
        },
      ]
    };
  },
  methods: {
    addItemToCart(product) {
      this.cart.push(product);
    },
    removeItemFromCart(product) {
      this.cart.splice(this.cart.indexOf(product));
    },
    navigateTo(page) {
    this.page = page;
  },
  }
};
</script>


<template>
  
  <div v-if="page === 'products'">
    <header class="cart">
    {{ cart.length }} in cart 
    <button class="viewcart" @click="navigateTo('cart')">View Cart</button>
    </header>
    <h1>New Collection</h1>
    <div class="newcollection">
    <div v-for="(product, index) in products" :key="index">
      <img :src="product.image"/>
      <button class="button" @click="addItemToCart(product)"> Add to Cart</button>
      <h4> {{ product.cost }} </h4>
      <h3> {{ product.name }} </h3>
      <hr>
    </div>   
    </div>
  </div>

  <div v-if="page === 'cart'">
    <header class="cart">
    {{ cart.length }} in cart 
    <button class="viewcart" @click="navigateTo('products')"> View Product</button>
    </header>
    <h1>My Shopping Cart</h1>
    <div class="products">
      <div v-for="(product, index) in cart" :key="index">
        <table>
          <tr>
            <td>Product's Name: </td>
            <td>{{ product.name }}</td>
            <td>|Price: </td>
            <td>{{ product.cost }}</td>
            <td><button class="remove" @click="removeItemFromCart">Remove</button></td>
        </tr>
        </table>
      </div>
    </div>
  </div>
  
</template>

<style>

table {
  text-align: center;
  margin-left: auto;
  margin-right: auto;
}

.cart {
  text-align: end;
  margin-right: 20px;
  margin-top: 10px;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;

}

.remove{
  display: inline-block;
  outline: 0;
  border: none;
  cursor: pointer;
  font-weight: 600;
  border-radius: 4px;
  font-size: 13px;
  height: 30px;
  background-color: #0000d0d;
  color: #0e0e10;
  padding: 0 10px;
  margin-left: 10px;
}

.remove:hover{
  background-color: lavenderblush;
}

.viewcart{
  display: inline-block;
  outline: 0;
  border: none;
  cursor: pointer;
  font-weight: 600;
  border-radius: 4px;
  font-size: 13px;
  height: 30px;
  background-color: #0000000d;
  color: #0e0e10;
  padding: 0 10px;
  margin-left: 10px;
}

.viewcart:hover {
    background-color: #0000001a;
}



h1 {
  text-align: center;
  font-family: fantasy;
}

img {
  width: 30%;
  margin-left: auto;
  margin-right: auto;
  display: block;
}

h3 {
  text-align: center;
  font-family: Comic Sans MS;
  font-size: 20px;
  margin-top: 0px;;
}

h4 {
  margin: 0%;
  margin-top: 10px;
  text-align: center;
}

hr{
  width: 40%;
  text-align: center;
  margin-top: 10px;
  margin-bottom: 10px;
}

.button{
  display: block;
  width: 30%;
  border: none;
  background-color: #59788E;
  color: white;
  padding: 14px 28px;
  cursor: pointer;
  text-align: center;
  margin-left: auto;
  margin-right: auto;
}

.button:hover{
  background-color: lightgrey;
  color: black;
}
</style>
