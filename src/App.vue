<template>
  <div class="app">
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
    <div class="post" v-for="post in posts" v-bind:key="post.id">
      <div><strong>Название:</strong> Пост о {{post.title}}</div>
      <div><strong>Описание:</strong> {{post.body}}</div>
    </div>
  </div>

</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data() {
    return {
      posts: [
        {id:1, title: "JavaScript", body: "Описание раз"},
        {id:2, title: "Java", body: "Описание два"},
        {id:3, title: "Python", body: "Описание три"},
      ],
      title: '',
      body: '',
    }
  },
  methods: {
    createPost () {
      this.posts.push({id: Date.now(),title: this.title, body: this.body})
      this.title = ''
      this.body = ''
    },
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.app {
  padding: 10px;
}
.post {
  margin-top: 10px;
  padding: 15px;
  border: solid #42b983 2px;
}
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
