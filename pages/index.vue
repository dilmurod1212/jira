<template>
  <div class="">
    <LayoutsMainNavbar />
    <div
      class="h-screen pt-[10vh] flex justify-between items-center bg-gradient-to-t from-white dark:from-black to-blue-600 dark:to-blue-800"
    >
      <div class="container flex flex-col gap-y-2">
        <h2 class="text-5xl">
          Move fast, stay aligned and build better - together
        </h2>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Corrupti quod
          iusto facilis alias? Illum voluptas eum corporis velit fugiat
          obcaecati.
        </p>
        <nuxt-link to="/auth" class="mt-2">
          <UButton label="Try it free" color="blue" size="xl" />
        </nuxt-link>
      </div>
      <NuxtImg src="hero.webp" />
    </div>
  </div>
</template>

<script setup lang="ts">
useHead({
  title: "Jira software",
});
definePageMeta({
  layout: "default",
});
</script>
