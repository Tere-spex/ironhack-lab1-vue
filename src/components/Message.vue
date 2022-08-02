<template>
<div>
    <h2>{{ message }}</h2>
    <button @click="helloWorld">Message</button>
</div>
</template>

<script>
export default {
  name: "message",
  data(){
    return{
        message: "",
    }
  },
  methods:{
    helloWorld(){
      this.message = "Hello World!!";
    },
  },
}
</script>

<style scoped>
    h2{
       color: blue;
    }
    button{
        padding: 5px 30px;
        background-color: rgb(20, 148, 107);
        color: white;
        font-size: 1.5rem;
        margin: 15px;
        border-radius: 25px;
    }
</style>