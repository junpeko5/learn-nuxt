<template>
  <div>
    <Nav />
    <div class="jumbotron"></div>
    <nuxt />
  </div>
</template>

<style>
  body {
    background: azure
  }
</style>

<script>
import Nav from '@/components/Nav'

export default {
  components: {
    Nav
  }
}
</script>
