<template>
  <div>
    <h1>Hello world</h1>
    <v-select v-model="selected" placeholder="Select Category" :options="['foo', 'bar']"></v-select>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selected: ''
    }
  }
}
</script>
