<script setup>

import { ref , onMounted} from 'vue'

const count = ref(0);

const name = ref('');

const lastName = ref("Asc")

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
function updateName(event , lastName){
   name.value = event.target.value + lastName;
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
<br> 
<br>


<input type="text" @input="updateName($event , lastName)" placeholder="Give me the name"></input>

<h1>{{ name }}</h1>

<br>

<h1>{{ count }}</h1>
</template>