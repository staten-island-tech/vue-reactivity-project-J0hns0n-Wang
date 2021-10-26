<template>
  <div id="app">
    <h1>Vegan Pizza Builder</h1>
    <div id="pizza-main">
      <div id="img-container">
        <img class="crust-img" src="./assets/crust.png">
        <img class="topping-img" v-for="topping in chosenTopping" :key="topping.id" :src="topping.image" >
           <!-- <img :src="image">  -->
      </div>
      <div id="ingredients">
           <p class="topping" v-for="(topping, index) in toppings" :key="topping.id"  @click="updateTopping(index)">{{topping.topping}} </p>
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
        topping:"Tomatoes",
        image:require("./assets/tomatoes.png")
      },
      {
        id: 7004,
        topping:"Black Olives",
        image:require("./assets/black-olives.png")
      },
       {
        id: 7005,
        topping:"Ranch",
        image:require("./assets/ranch.png")
      }
    ],
    selectedTopping: 0,


    }
  },
  methods:{
    updateTopping(index){
      this.selectedTopping = index
      console.log(index)
      this.chosenTopping.push(this.toppings[index])
      console.log(this.chosenTopping)
    }
  },

  
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
  width: 40%;
  justify-content: space-around;
}

.topping{
  height: 4rem;
  width: 7rem;
  margin-top: 5px;
  background-color: rgba(192, 192, 192, 0.602);
  cursor: pointer;
  border-radius: 0.5rem;
  display: flex;
  flex-direction: column;
  text-align: center;
}

.crust-img{
  position: absolute;
  height: 70%;
  top: 0;
  left: 0;
  /* transform: translate(-7.75%, 2%); */
  transform: translateX(-11%);
}
.topping-img{
  position: absolute;
  height: 70%;
  top: 0;
  left: 0;
}


</style>
