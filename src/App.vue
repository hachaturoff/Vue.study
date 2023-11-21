
<template>
  <div class="app">
    <PostForm
        @create="createPost"
    />
    <PostList
        :posts="posts"
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
    }
  },
  methods: {
    createPost(post) {
      this.posts.push(post)
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
