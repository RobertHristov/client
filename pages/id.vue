<template>
  <div>
    <h1>{{ post.title }}</h1>
    <p>{{ post.body }}</p>
  </div>
</template>

<script>
  export default {
    async asyncData({ params, $http }) {
      const post = await $http.$get(`https://jsonplaceholder.typicode.com/posts/${params.id}`)
      return { post }
    }
  }
</script>

<style>

</style>