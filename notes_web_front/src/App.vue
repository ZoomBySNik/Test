<template>
  <div class="app">
    <post-form/>
    <post-list v-model:posts="posts"/>
    
  </div>
</template>

<script>
import PostList from "@/components/PostList";
import PostForm from "@/components/PostForm";
export  default {
  components: {
    PostList, PostForm
  },
  data(){
    return{
      components:{
        PostForm, PostList,
      },
      posts:[
        {id:1, title: 'JavaScript', body:'JavaScript is the good language'},
        {id:2, title: 'JavaScript 2', body:'JavaScript is the good language 2'},
        {id:3, title: 'JavaScript 3', body:'JavaScript is the good language 3'}
      ],
      title: '',
      body: '',
    }
  },
  
  methods:{
   createPost(){
     const newPost = {
       id: Date.now(),
       title: this.title,
       body: this.body,
     }
     this.posts.push(newPost);
     this.title = '';
     this.body = '';
   },
  }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
form{
  display: flex;
  flex-direction: column;
}
.app{
  padding: 20px;
}

</style>