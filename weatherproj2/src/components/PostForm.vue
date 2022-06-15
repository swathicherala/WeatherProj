<template>
  <div>
    <div class="container mb-4" style="max-width:400px;">
        <h1>Post Data</h1>
        <form @submit="postData" method="post">
       <input type="text" class="form-control" name="author" v-model="posts.author" placeholder="Author Name"/><br>
       <input type="text" class="form-control" name="title" v-model="posts.title" placeholder="Title"/><br>
       <button type="submit">Post</button>
    </form>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
 name:'PostForm',
 data(){
    return{
        posts:{
            author:"",
            title:""
        }
    }
 },
 methods:{
    async postData(e){
        let result = await axios.post("http://localhost:3000/posts",
          this.posts
      )
       e.preventDefault()
    }
 }
}
</script>

<style>

</style>