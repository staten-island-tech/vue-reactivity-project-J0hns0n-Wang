<template>
  <div id="app">
    <h1>Pizza Builder</h1>
  <button class="ingredients" v-for="topping in toppings" :key="topping">{{topping}}</button>

  </div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return{
    toppings:["Pepperoni",
"Mushroom",
"ExtraCheese",
"Sausage",
"Onion",
"BlackOlives",
"GreenPepper",
"FreshGarlic",
"Tomato",
"FreshBasil"],

    }
  },
  methods:{

  }
  
}
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
