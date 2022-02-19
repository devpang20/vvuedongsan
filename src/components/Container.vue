<template>
  <div>
    <Post v-for="(post, i) in postData" :key="i" :post="post" />
  </div>
</template>

<script>
import Post from './Post'

export default {
  name: 'container',
  components: {
    Post
  },
  props: {
    postData: Array,
  }
}

</script>

<style>

</style>
