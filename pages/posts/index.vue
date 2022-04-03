<template>
  <div>
    <p v-if="$fetchState.pending">Fetching posts...</p>
    <p v-else-if="$fetchState.error">An error occurred :(</p>
    <div v-else>
      <h1 class="text-3xl font-bold tracking-tight text-gray-900">Blog posts</h1>
        <div v-for="post in posts" :key="post.id">
          <NuxtLink :to="'/posts/'+ post.id">{{ post.title }}</NuxtLink>
        </div>
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