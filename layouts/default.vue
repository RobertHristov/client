<template>
  <div
    class="flex flex-col min-h-screen max-w-3xl mx-auto px-4 divide-y divide-gray-300"
  >
    <div class="pt-6 pb-4 text-center">
      <div class="flex items-center justify-center space-x-3">
        <NuxtLink to="/pages" aria-label="HomePage">
          <h1 class="text-3xl font-extrabold text-gray-900 tracking-tight">
            Blog website
          </h1>
        </NuxtLink>
      </div>

      <p class="text-xs text-gray-500 mt-1">by Robert Hristov</p>

      <nav class="mt-7">
        <ul class="flex items-center justify-center space-x-5">
          <li>
            <NuxtLink to="/" class="nav-link" aria-label="HomePage">
              Home
            </NuxtLink>
          </li>
          <li>
            <NuxtLink to="/posts" class="nav-link" aria-label="About page">
              Posts
            </NuxtLink>
          </li>
        </ul>
      </nav>
    </div>

    <main class="flex-grow py-10">
      <Nuxt />
    </main>

    <footer class="text-center py-5 text-gray-500 text-sm">
      Some footer
    </footer>
  </div>
</template>

<style lang="postcss" scoped>
.nav-link {
  @apply text-green-700 hover:text-green-800 underline;
}
</style>