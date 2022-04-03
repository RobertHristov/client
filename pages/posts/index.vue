<template>
  <div>
    <h1 class="text-3xl font-bold tracking-tight text-gray-900">Blog posts</h1>
    <div v-for="post in posts" :key="post.id">
      <NuxtLink :to="'/posts/'+ post.id" class="font-light leading-7 text-gray-500 text-lg">
      {{ post.title }}
      </NuxtLink>
    </div>
  </div>
</template>

<script>
// Get all the posts from the API.
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