<template>
  <div id="app">
<body>
    <div id="app">
        <header>
            <h1>{{ message }}</h1>
            <h2>Menu: </h2>
            <Menu v-for= "item in this.simpleMenu" :v-if= "inStock">
                <img :src="item.image.source" :alt= "item.image.alt"/>
            </br>
                <b>Nom: {{ item.name }} </b>
            </br>
                quantité: {{ item.quantity }}

                
            <button @click= "addToShoppingCart">Ajouter ce produit dans le panier</button>
            </Menu>
            <p :v-else-if= "inStock = false" >Produits non existant dans le stock</p>
            <h1 v-model= "cartTotal"> {{ cartTotal }}</h1>
        </header>
        <footer>{{ copyright }}</footer>
    </div>

    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
  
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Menu from "./components/Menu.vue"
export default {
  name: 'App',
  components: {
    HelloWorld,
    Menu
  }
}
  const app = new Vue({
      el: "#app",
      data: {
          message: "Bonjour 👋 ",
          restaurantName: "Paradise",
          Numero_de_téléphone: "0687457899",
          Email: "paradise@gmail.com",
          Adresse_postale: 8000,
          cartTotal : 0
      },

      computed: {
          copyright(){
              const currentYear = new Date().getFullYear()
              return "@copyright "+ this.restaurantName + " " + currentYear
          }
      },
      methods: {
          addToShoppingCart(){
                  this.cartTotal += 1                    
          }
      }
  });
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
