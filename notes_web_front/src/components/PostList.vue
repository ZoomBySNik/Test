<template>
  <div class="post" v-for="post in posts">
    <div><strong>Title </strong>{{post.title}}</div>
    <div><strong>Description </strong>{{post.body}}</div>
  </div>
</template>

<script>
export default {
  props:{
    posts: {
      type: Array,
      required: true,

    }
  }
}
</script>

<style scoped>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.post{
  padding: 15px;
  border: 3px solid gray;
  margin-top: 15px;
}
</style>