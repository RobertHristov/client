<template>
    <div class="w-full pl-14">
        <div class="flex justify-between items-center mb-6">
            <h1 class="text-2xl font-bold">{{post.title}}</h1>
        </div>
        <p class="leading-loose mb-5">
            {{ post.body }}
        </p>
    </div>
</template>

<script>
// Get a single post from the API using post ID.
  export default {
    async asyncData({ params, $axios }) {
        const post = await $axios.$get(`https://jsonplaceholder.typicode.com/posts/${params.id}`)
        return { post }
    } 
  }

</script>

<style>

</style>