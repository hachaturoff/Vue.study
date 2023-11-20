


<script setup>
import {onMounted, ref} from 'vue'

let visible = ref(true)

const trigger = function() {
      visible.value = visible.value ? false : true
    }

onMounted(() => {})


</script>

<style scoped>
</style>

<template>
  <div>
    <button @click="trigger">change</button>
    <p v-if="visible">Hallo</p>
  </div>
</template>

