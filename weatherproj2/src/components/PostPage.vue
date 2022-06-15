<template>
  <div>
    <div class="container mb-4" style="max-width:400px;">
        <h1 class="text-center mb-4">Login Form</h1>
        <form @submit.prevent="postData" method="post">
       <input type="email" class="form-control" name="email" v-model="data.email" placeholder="Email"/><br>
       <input type="password" class="form-control" name="password" v-model="data.password" placeholder="Password"/><br>
       <button class="btn btn-primary" style="width:100%">Submit</button>
    </form>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
 name:'PostPage',
 data(){
    return{
       
            data:{
                email:"",
            password:""
        
            }
    }
 },
 methods:{
    async postData(){
       // console.log(this.email,this.password)
        let result=await axios.post("http://localhost:3000/posts",
          this.data)
       console.log("result",result)
    }
 }
}
</script>

<style>

</style>