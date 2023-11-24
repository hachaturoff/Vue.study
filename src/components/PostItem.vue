<template>

  <div class="post" >
    <div>
      <div><strong>Название:</strong> Пост о {{ post.title }}</div>
      <div><strong>Описание:</strong> {{ post.body }}</div>
    </div>
    <div class="post__btns">
      <MyButton @click="deletePost">Удалить</MyButton>
    </div>
  </div>
</template>

<script>

export default {

  name: "PostItem",
  props: {
    post: {
      type: Object,
      required: true,
    }
  },
  methods: {
    deletePost() {
      this.$emit('delete', this.post.id)
      // console.log(this.post.id)
    }
  }
}
</script>

<style scoped>
.post {
  margin-top: 10px;
  padding: 15px;
  border: solid #42b983 2px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>
