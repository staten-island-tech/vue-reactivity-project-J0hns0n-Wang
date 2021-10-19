<template>
  <div id="app">
    <h1>Pizza Builder</h1>
    <div id="pizza-main">
         <img :src="image"> 
      <div id="ingredients">
           <button class="topping" v-for="topping in toppings" :key="topping">{{topping}}</button>
      </div>

    </div>
 

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

image:"test-pizza.png"
    }
  },
  methods:{

  }
  
}
</script>

<style lang="css">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

#ingredients{
  display: flex;
  width: 80vw;
  justify-content: space-around;
}


</style>
