<template>
  <div>
    <h2>Making API request - the Vue way</h2>
    <div class="container">
      <div class="row">
        <Card v-for="post in posts" :key="post.id" :post="post" class="ml-auto mr-auto" />
        <button class="btn btn-danger" v-scroll-to="'body'">Back to Top</button>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import Card from '@/components/Card'
import {mapGetters} from 'vuex'

export default {
  components: {
    Card
  },
  data() {
    return {
      allPosts: ''
    }
  },
  computed: {
    ...mapGetters(['posts'])
  },
  head: {
    title: 'List of Posts'
  }
}
</script>
