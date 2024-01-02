<template>
  <div
    class="h-[80px] w-full fixed top-0 left-0 z-50 bg-gray-100 dark:bg-gray-900 my-auto"
  >
    <div class="container flex items-center justify-between h-full w-full">
      <nuxt-link to="/" class="flex items-center space-x-1">
        <NuxtImg src="logo.svg" width="50" height="50" />
        <span class="text-2xl">Jira Software</span>
      </nuxt-link>
      <div class="flex items-center gap-x-2">
        <SharedColorMode />
        <nuxt-link to="/auth">
          <UButton color="blue">Get it free</UButton>
        </nuxt-link>
        <nuxt-link to="/auth">
          <UButton color="blue" variant="outline">Sign</UButton>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>
