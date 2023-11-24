<template>
  <div class="postList" v-if="posts.length > 0">
    <h3>Список Постов</h3>
    <PostItem
        v-for="post in posts"
        :post="post"
        :key="post.id"
        @remove="$emit('remove', post)"
    />
  </div>
  <h2 v-else style="color: red">
    Список постов Пуст
  </h2>
</template>

<script>
import PostItem from "@/components/PostItem";
export default {
  name: "PostList",
  components: {
    PostItem
  },
  props: {
    posts: {
      type: Array,
      required: true,
    }
  },
  methods: {
    // deletePost(id) {
    //   this.$emit('delete', id)
    // }
  }
}

// console.log(this.props)
</script>

<style scoped>
.postList {
  margin-top: 20px;
}
</style>
