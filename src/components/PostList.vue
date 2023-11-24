<template>
  <div>
    <h3>Список пользователей</h3>
    <PostItem
        v-for="post in posts"
        :post="post"
        :key="post.id"
        @delete="deletePost"
    />
  </div>
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
    deletePost(id) {
      this.$emit('delete', id)
    }
  }
}

// console.log(this.props)
</script>

<style scoped>

</style>
