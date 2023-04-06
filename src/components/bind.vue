<script setup>
import { ref } from 'vue'
const url= ref("https://yesno.wtf/api")
 

async function reload() {
  const result= await fetch("https://yesno.wtf/api")
     url.value=await result.json()

}

</script>

<template>
<button @click="reload">result</button>
<p>
  {{ url.answer }}
</p>
<img :src="url.image">


</template>