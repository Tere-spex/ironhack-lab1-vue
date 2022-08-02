<template>
<div>
  <h1>This is a Counter Component</h1>
  <h2 :class="{
    'green': counter <= max - 5,
    'orange': counter >= max - 4 && counter <= max - 2,
    'red': counter > max - 2,
  }">
  {{ counter }}</h2>
  <button @click="decrease">-1</button>
  <button @click="increase">+1</button>
</div>
</template>

<script>
export default {
  name: "counter",
  props: ["max"],
  data() {
    return{
      counter: 0,
    }
  },
  methods:{
    decrease(){
      if (this.counter > 0) this.counter--;
    },
    increase(){
      if (this.counter < this.max) this.counter++;
    },
  },
};
</script>

<style scoped>
 div{
  background-color: rgb(231, 240, 237);
  padding: 25px;
 }
 button{
  padding: 5px 30px;
  background-color: rgb(20, 148, 107);
  color: white;
  font-size: 1.5rem;
  margin: 15px;
  border-radius: 25px;
 }
.red{
  color: red;
}
.orange{
  color: orange;
}
.green{
  color: rgb(10, 207, 10);
}
</style>
