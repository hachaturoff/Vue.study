<template>
  <img alt="Vue logo" src="./assets/logo.png">
<!--  <HelloWorld msg="Welcome to Your Vue.js App"/>-->
  <TimeBox msg="Тут будет время" />
  <ItemBox data={{[1,2,3]}} />
<!--  <IncrementBtn  />-->
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import TimeBox from './components/TimeBox.vue'
import ItemBox from './components/ItemBox.vue'
// import IncrementBtn from './components/IncrementBtn.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    TimeBox,
    ItemBox
    // IncrementBtn
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
