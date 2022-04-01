<template>
  <div>
    <p v-if="$fetchState.pending">Fetching mountains...</p>
    <p v-else-if="$fetchState.error">An error occurred :(</p>
    <div v-else>
      <h1>Blog posts</h1>
      <ul>
        <li v-for="post of posts" :key="post.id">{{ post.title }}</li>
      </ul>
      <button @click="$fetch">Refresh</button>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        posts: []
      }
    },
    async fetch() {
      this.posts = await fetch(
        'https://jsonplaceholder.typicode.com/posts/'
      ).then(res => res.json())
    }
  }
</script>

<style>

</style>