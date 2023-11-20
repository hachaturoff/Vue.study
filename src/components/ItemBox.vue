


<script setup>
import {onMounted, ref} from 'vue'
// export default {
//   name: "ItemBox",
//   props: {
//     msg: String
//   },
//   data() {
//     return {
//       visible: true,
//
//     }
//   },
//   methods: {
//     trigger: function() {
//       this.visible = this.visible ? false : true
//       // console.log(this.visible)
//     }
//   }
// }
let visible = ref(true)

const trigger = function() {
      visible.value = visible.value ? false : true
      // console.log(visible)
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

