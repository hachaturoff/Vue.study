<template>
  <h2 id="h2">{{cr}}</h2>
  <button v-on:click='icrement'>++++</button>
  <button v-on:click='dicrement'>----</button>
</template>

<script>
export default {
  name: "IncrementBtn",
  data: function () {
    return {
      cr: 0
    }
  },
  methods: {
    icrement: function () {
      this.cr++
    },
    dicrement: function () {
      this.cr--
    }
  }
}
</script>

<style scoped>

</style>