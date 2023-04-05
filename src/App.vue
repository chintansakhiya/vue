<script setup>
import { reactive, ref } from 'vue'

const counter = reactive({ count: 0 })

const red= ref('colors')
const count=ref(0)
function incress() {
count.value++  
}
</script>

<template>
  <h1 :class="red">Hello World!</h1>
  <p>Count is: {{ count }}</p>
  <button @click="incress">Count</button>
</template>

<style scoped>
 .colors{
  color: red;

 }
</style>
