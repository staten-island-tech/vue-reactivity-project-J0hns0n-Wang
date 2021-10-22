<template>
  <div id="app">
    <h1>Pizza Builder</h1>
    <div id="pizza-main">
      <div id="img-container">
        <img class="crust-img" src="./assets/test-pizza-removebg-preview.png">
        <img class="topping-img" v-for="(topping, index) in toppings" :key="topping.id" @click="addTopping(index)">
           <!-- <img :src="image">  -->
      </div>
      <div id="ingredients">
           <button class="topping" v-for="topping in toppings" :key="topping">{{topping.topping}}</button>
      </div>

    </div>
 

  </div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return{
      chosenTopping:[],
    toppings:[
      {
        id: 7000,
        topping:"Green Peppers",
        image:require("./assets/green-peppers.png")
      },
       {
        id: 7001,
        topping:"Mushrooms",
        image:require("./assets/mushrooms.png")
      },
       {
        id: 7002,
        topping:"Onions",
        image:require("./assets/onions.png")
      },
       {
        id: 7003,
        topping:"Pepperoni",
        image:require("./assets/pepperoni1.png")
      }, {
        id: 7004,
        topping:"Ranch",
        image:require("./assets/ranch.png")
      }
    ],
    selectedTopping: 0,


    }
  },
  methods:{
    addTopping: function(index){
      this.selectedTopping = index
      // console.log(index)
    }
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

.crust-img{
  position: absolute;
  height: 20rem;
  top: 0;
  left: 0;
}
.topping-img{
  position: absolute;
  height: 20rem;
  top: 0;
  left: 0;
}


</style>
