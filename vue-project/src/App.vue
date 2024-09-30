<script setup>

import { ref , onMounted} from 'vue'

const count = ref(0);

function increment(){
  count.value++;
}

onMounted(()=>{
  console.log(`This is the count ${count.value}`);
})
</script>

<template>
<button @click="increment"> Count is {{ count }}</button>
</template>