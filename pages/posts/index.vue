<template>
  <div>
    <h2>Making API request - the Vue way</h2>
    <div class="container">
      <h4 v-for="post in posts" :key="post.id">
        {{ post.title }}
      </h4>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  data() {
    return {
      posts: ''
    }
  },
  asyncData() {
    return axios.get('https://jsonplaceholder.typicode.com/todos')
        .then(res => {
          return {
            posts: res.data
          }
        })
        .catch(error => {
          console.log(error)
        })
  }
}
</script>
