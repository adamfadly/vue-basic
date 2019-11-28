<template>
  <div id="blogs">
    <h2>{{ titleBlog}}</h2>
    <input type="text" v-model="searchTerm">
    <div v-for="post in filteredPosts" :key="post.id">
       <h2>{{ post.title }}</h2>
       <p>{{ post.body | snippet }}</p>
    </div>
  </div>
</template>


<script>
import axios from 'axios'

export default {
  name: 'blogs',
  data () {
    return {
      titleBlog: 'This Blogs and using API to display',
      posts: [],
      searchTerm: ''
    }
  },
  methods: {

  },
  computed : {
    filteredPosts() {
      return this.posts.filter(post => {
        return post.title.match(this.searchTerm)
      })
    }
  },

  created() {
    axios.get('https://jsonplaceholder.typicode.com/posts/')
    .then(response => {
      console.log(response)
      this.posts = response.data
    }).catch(err => {
      console.log(err)
    })
  }
}
</script>


<style>

input {
  background-color: #ddd;
  width: 200px;
}

</style>
