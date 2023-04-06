<script setup>
import imgss from './components/bind.vue'
import watcherExample from './components/watcher.vue'
import formExample from './components/form.vue'
const x="dd"

</script>

<template>

  <h1>vue:)</h1>
  <imgss />
  <hr>
  <watcherExample />
  <hr>
  <formExample />
  <hr>
</template>




<!-- <script setup>
import { ref,computed } from 'vue'

let id = 0

const newTodo = ref('')
const hideCompleted = ref(false)
const todos = ref([
  { id: id++, text: 'Learn HTML', done: true },
  { id: id++, text: 'Learn JavaScript', done: true },
  { id: id++, text: 'Learn Vue', done: false }
])

function addTodo() {
  todos.value.push({ id: id++, text: newTodo.value, done: false })
  newTodo.value = ''
}
 
const filterdata = computed(()=>{return hideCompleted.value?todos.value.filter((t)=>!t.done):todos.value})

function removeTodo(todo) {
  todos.value = todos.value.filter((t) => t !== todo)
}
</script>

<template>
  <form @submit.prevent="addTodo">
    <input v-model="newTodo">
    <button>Add Todo</button>
  </form>
  <ul>
    <li v-for="todo in filterdata" :key="todo.id">
      <input type="checkbox" v-model="todo.done">
      <span :class="{ done: todo.done }">{{ todo.text }}</span>
      <button @click="removeTodo(todo)">X</button>
    </li>
  </ul>
  <button @click="hideCompleted = !hideCompleted">
    {{ hideCompleted ? 'Show all' : 'Hide completed' }}
  </button>
</template>

<style>
.done {
  text-decoration: line-through;
}
</style> -->

<!-- -------------------------------------------------------------------- -->

<!-- <script setup>
import { ref, onMounted,onUnmounted,onUpdated } from 'vue'

const p = ref("nullhsshhd")
let k=ref(true)
setInterval(() => {p.value += "l";k.value=!k.value}, 215)



 
 onMounted(() => {
  console.log("mounted",Date.now());
  
})
onUpdated(() => {
  console.log("onUpdated",Date.now());
  
})
  
 onUnmounted(() => {
  console.log(`unmounte ${Date.now()}`);
  
})
</script>

<template>
  <p v-if="k">{{p}}</p>
</template> -->

<!---------------------------------------------------------------------->
