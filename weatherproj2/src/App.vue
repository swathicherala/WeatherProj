<template>
  <div class="main">
   <PostPage />
  </div>
</template>

<script>
import PostPage from './components/PostPage'
import axios from 'axios'
export default {
  name: 'App',
  components:{
    PostPage
  }
}
</script>

<style>

</style>
