<template>
  <div>
    <Nav />
    <nuxt />
  </div>
</template>

<style>
body {
  background-color: azure;
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
