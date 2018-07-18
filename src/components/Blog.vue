<template>
  <div class="content">
    <div id="blog">
      <h2>Blog Posts</h2>
      <input type="text" v-model="searchTerm">
      <div v-for="post in filteredPosts" :key="post.id">
        <h3>{{ post.title }}</h3>
        <p>{{ post.body | snippet }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'Blog',
  data() {
    return {
      posts: [],
      searchTerm: ''
      }
    },
  methods: {  },
  computed: {
    filteredPosts() {
      return this.posts.filter(post => {
        return post.title.match(this.searchTerm)
      })
    }
  },
  created() {
    // const posts = axios.get('http://localhost:3000/posts/')
    const posts = axios.get('https://jsonplaceholder.typicode.com/posts/')
    .then(response => {
      // console.log(response)
      this.posts = response.data
    })
    .catch(err => {
      console.log(err)
    })
  }
}
</script>

<style>
p {
  color: #444;
}
</style>

