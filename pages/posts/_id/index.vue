<template>
    <p v-if="$fetchState.pending">Loading...</p>
    <p v-else-if="$fetchState.error">Error! :(</p>
    <div v-else class="flex">
        <div class="w-full pl-14">
            <div class="flex justify-between items-center mb-6">
                <h1 class="text-2xl font-bold">{{post.title}}</h1>
            </div>
            <p class="leading-loose mb-5">
                {{ post.body }}
            </p>
        </div>
    </div>
</template>

<script>

  export default {
    async asyncData({ params, $axios }) {
        const post = await $axios.$get(`https://jsonplaceholder.typicode.com/posts/${params.id}`)
        return { post }
    } 
  }

</script>

<style>

</style>