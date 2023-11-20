<template>
  <div class="post" v-for="post in posts" v-bind:key="post.id">
    <div><strong>Название:</strong> Пост о {{post.title}}</div>
    <div><strong>Описание:</strong> {{post.body}}</div>
  </div>
</template>

<script>
export default {
  name: "PostList",
  props: {
    posts: {
      type: Array,
      required: true,
    }
  }
}
</script>

<style scoped>
.post {
  margin-top: 10px;
  padding: 15px;
  border: solid #42b983 2px;
}
</style>