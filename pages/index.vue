<template>

<div id="app">

  <div class="heading">
    <h2>Counter app </h2>
  </div>

  <div class="btn">
    <button @click="increment">+1</button>
    <button @click="alertCounter" >say 1</button>
    <button @click="decrement" >-1</button>
  </div>

 <div class='display'>
    <h1 class="number">Count is {{count}}</h1>
  </div>

  </div>

</template>


<script  setup>
import { ref } from 'vue'

// reactive state
const count = ref(0)

// functions that mutate state and trigger updates
function increment() {
  count.value++;
}

function alertCounter() {
   alert(`Count is ${count.value}`);
}

function decrement() {
  count.value--;
}


</script>



 

<style>

body{
    background-color:aliceblue;
}

.heading{
    display: flex;
    justify-content:center;
    align-items: center;
    margin-top: 2rem;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.btn{
        display: flex;
    justify-content:center;
    align-items: center;
    gap: 2rem;
}

.number{
     display: flex;
    justify-content:center;
    align-items: center;
    font-size: 5rem;
}
</style>
