<template>

  <div class="time">
    <h1>
      Тут будет время
    </h1>
    <h2>
      {{text1}}
    </h2>
  </div>

</template>

<script>
export default {
  name: "TimeBox",
  props: {
    msg: Array
  },
  data() {
    return {
      text1: (() => {
        let today = new Date();
        const dd = String(today.getDate()).padStart(2, '0');
        const mm = String(today.getMonth() + 1).padStart(2, '0'); //January is 0!
        const yyyy = today.getFullYear();

        today = mm + '/' + dd + '/' + yyyy;
          return today
      })(),
      text2: '222',
    }
  }
}
</script>

<style scoped>

</style>