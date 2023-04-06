<script setup>
import { ref, watch } from 'vue'

const counter = ref(0)
const result = ref("")


// watch works directly on a ref
// watch(counter, async (newQuestion, oldQuestion) => {
//   if (newQuestion.indexOf('?') > -1) {
//     answer.value = 'Thinking...'
//     try {
//       answer.value = (await res.json()).answer
//     } catch (error) {
//       answer.value = 'Error! Could not reach the API. ' + error
//     }
//   }

// })
watch(counter, () => {
    changeID()
})

async function changeID() {
    const res = await fetch(`https://jsonplaceholder.typicode.com/todos/${counter.value}`)
    result.value = await res.json()

}
</script>

<template>
    <br>
    <button @click="counter++">incress ID</button>

    <p>
        {{ result.id }} <br>
        {{ result }} <br>
    </p>
</template>