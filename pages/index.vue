<script setup>

let number= 0;

function incrementCounter() {
 document.querySelector('.number').innerHTML = ++number;
}

function decrementCounter() {
 document.querySelector('.number').innerHTML = --number;
}
    
function alertCounter() {
  console.log(alert(`the number is ${number}`))
}

</script>

<template>
  <div class="heading">
    <h2>Counter app </h2>
  </div>
  <div class="btn">
    <button @click="incrementCounter"   class='increment' type="submit">+1</button>
    <button @click="alertCounter" class='alert' type="submit">say 1</button>
    <button @click="decrementCounter" class='decrement' type="submit">-1</button>
  </div>

  <div class='display'>
    <h1 class="number">{{number}}</h1>
  </div>

</template>



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
