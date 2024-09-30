<script setup>

import { ref , onMounted} from 'vue'

const count = ref(0);

function increment(){
  count.value++;
}

function decrement(){
  count.value--;
}
 function increment_number(number){

    count.value+=number;

 }

 function decrement_number(number){
   count.value-=number;
 }

onMounted(()=>{
  console.log(`This is the count ${count.value}`);
})
</script>

<template>
<button @click="increment">Inc  Count is {{ count }}</button>

<button @click="decrement">Dec Count is {{ count }}</button>

<button @click="increment_number(5)">Inc count Count is </button>

<button @click="decrement_number(5)"> Decrement Count is </button>  

<h1>{{ count }}</h1>
</template>