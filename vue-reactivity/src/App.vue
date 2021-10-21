<template>
  <div id="app">
    <h1>Pizza Builder</h1>
    <div id="pizza-main">
      <div id="img-container">
        <img class="crust-img" src="./assets/test-pizza-removebg-preview.png">
           <!-- <img :src="image">  -->
      </div>
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
    toppings:[
      "Green Peppers",
      "Mushrooms",
      "Onions",
      "Pepperoni",
      "Ranch"
    ],


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
}
#img-container{
  width: 50%;
}
#pizza-main{
  display: flex;
  flex-direction: row;

}
#ingredients{
  display: flex;
  /* width: 80vw; */
  justify-content: space-around;
}

.topping{
  height: 2rem;
  cursor: pointer;
}


</style>
