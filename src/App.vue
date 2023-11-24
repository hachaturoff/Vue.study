
<template>
  <div class="app">
    <h1>Страница с постами</h1>
    <MyButton
      @click="showDialog">
      Добавить Пост
    </MyButton>
    <MyDialog
        v-model:show="this.dialogVisible" >
      <PostForm
          @create="createPost"
      />
    </MyDialog>
    <PostList
        :posts="posts"
        @remove="deletePost"
    />

  </div>

</template>

<script>
import PostForm from "@/components/PostForm";
import PostList from "@/components/PostList";

export default {
  name: 'App',
  components: {
    PostForm,
    PostList
  },
  data() {
    return {
      posts: [
        {id:1, title: "JavaScript", body: "Описание раз"},
        {id:2, title: "Java", body: "Описание два"},
        {id:3, title: "Python", body: "Описание три"},
      ],
      dialogVisible: true
    }
  },
  methods: {
    createPost(post) {
      this.posts.push(post),
      // console.log('sda')
      this.dialogVisible = false
    },
    deletePost(post) {
      this.posts = this.posts.filter(item => item.id !== post.id)
    },
    showDialog() {
      this.dialogVisible = true
    }
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

</style>
