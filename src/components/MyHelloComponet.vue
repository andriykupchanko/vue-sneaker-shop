<script setup> 
import  {ref} from 'vue' 

const count = ref(0)

function increment(){
count. value++
console. log (count)
}

function updatedCounter(event) {
    count.value = Number(event.target.value);
}
</script>
<template>
    <h1>{{ count }}</h1>
    <button @click="increment">+</button>
    <input @input="updatedCounter"/>
</template>