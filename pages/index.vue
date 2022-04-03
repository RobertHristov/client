<template>
  <ul class="divide-y divide-gray-300 -mt-10">
    <li class="py-14">
      <article>
        <div class="space-y-5">
          <NuxtLink to="#">
            <h2 class="text-3xl font-bold tracking-tight text-gray-900">
              The place where you can find blog posts
            </h2>
          </NuxtLink>
          <p class="font-light leading-7 text-gray-500 text-lg">
            If you want to check some blog posts, please click on "Details"
          </p>

          <div class="mt-5">
            <NuxtLink
              to="#"
              class="font-medium text-green-600 hover:text-green-700"
            >
              Details →
            </NuxtLink>
          </div>
        </div>
      </article>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'HomePage'
}
</script>
