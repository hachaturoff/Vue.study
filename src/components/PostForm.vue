<template>
  <form @submit.prevent>
    <h4>Создание Поста</h4>
    <MyTextInput
        v-model="post.title"
        type="text"
        placeholder="Название"/>
    <MyTextInput
        v-model="post.body"
        type="text"
        placeholder="Описание"/>
    <MyButton @click="createPost">Добавить</MyButton>
  </form>
</template>

<script>
export default {
  name: "PostForm",
  data() {
    return {
      post: {
        title: '',
        body: ''
      }
    }
  },
  methods: {
    createPost () {
      this.post.id = Date.now(),
      this.$emit('create', this.post)
      this.post = {
        title : '',
        body : ''
      }
    },
  }
}
</script>

<style scoped>
form {
  padding: 15px;
  /*border: solid #95b942 2px;*/
}
form * {
  margin-top: 10px;
}
input{
  width: 100%;
}
</style>
