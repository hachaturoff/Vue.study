



<script setup>
import { ref, onMounted } from 'vue'

// reactive state
const count = ref('')
const text = ref('')

// functions that mutate state and trigger updates
// function increment() {
//   count.value++
// }

function getDay(textin) {
  count.value = textin
}

// lifecycle hooks
onMounted(() => {
  // console.log(`The initial count is ${count.value}.`)

})

</script>

<template>
  <input v-model="text" class="inputDay" type="text">
  <div>{{count}}</div>
  <button v-on:click='getDay(text)'>+++</button>
</template>

<style scoped>

</style>