<template>
  <form @submit.prevent>
    <h5>Creating of the post</h5>
    <input
        v-model="post.title"
        class="input"
        type="text"
        placeholder="Title"
    >
    <input
        v-model="post.body"
        class="input"
        type="text"
        placeholder="Description"
    >
    <button
        class="button"
    >
      Create
    </button>
  </form>
</template>

<script>
export default {
  data(){
    return{
      post: {
        title: '',
        body: '',

      }
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
.input{
  width: 100%;
  border: 1px solid red;
  padding: 10px 15px;
  margin-top: 5px;
}
.button{
  margin-top: 15px;
  align-self: self-end;
  padding: 10px 15px;
  border-color: cyan;
  background: none;
}
</style>