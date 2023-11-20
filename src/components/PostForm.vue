<template>
  <form @submit.prevent>
    <h4>Создание Поста</h4>
    <input
        v-bind:value="title"
        @input="title = $event.target.value"
        type="text"
        placeholder="Название">
    <input
        v-bind:value="body"
        @input="body = $event.target.value"
        type="text"
        placeholder="Описание">
    <button @click="createPost">Добавить</button>
  </form>
</template>

<script>
export default {
  name: "PostForm",
}
</script>

<style scoped>
form {
  padding: 15px;
  border: solid #95b942 2px;
}
form * {
  margin-top: 10px;
}
input{
  width: 100%;
}
</style>