<template>
  <main class="">
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
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Corrupti
            quod iusto facilis alias? Illum voluptas eum corporis velit fugiat
            obcaecati.
          </p>
          <nuxt-link to="/auth" class="mt-2">
            <UButton label="Try it free" color="blue" size="xl" />
          </nuxt-link>
        </div>
        <NuxtImg src="hero.webp" />
      </div>
    </div>
    <section class="container py-6">
      <h2 class="text-4xl">All from a single source of truth</h2>
      <UTabs
        :items="tabs"
        class="my-4"
        :ui="{ list: { width: 'w-fit' } }"
        :default-index="2"
      >
        <template #item="{ item }">
          <div class="flex items-center justify-between">
            <div class="w-[40%]">
              <h2 class="text-3xl font-medium">{{ item.label }}</h2>
              <p>{{ item.description }}</p>
              <div
                class="py-4 mt-12 rounded-r-full flex flex-col space-y-2 bg-gradient-to-r from-white dark:from-black to-blue-600 dark:to-blue-800"
              >
                <UIcon name="bxs:quote-alt-left" class="text-4xl" />
                <p class="text-lg pl-2">{{ item?.credentials.text }}</p>
                <div class="pl-2 opacity-65">
                  <p class="font-bold">{{ item?.credentials.username }}</p>
                  <p class="text-xs">{{ item?.credentials.company }}</p>
                </div>
              </div>
            </div>
            <NuxtImg :src="item.image" class="w-[55%]" />
          </div>
        </template>
      </UTabs>
    </section>
    <section class="container">
      <h2 class="text-center text-4xl font-medium">Easier than eveer</h2>
      <div class="flex items-center justify-between mx-auto max-w-xl py-2">
        <div class="h-12 w-12 rounded-full bg-blue-500 dark:bg-blue-800"></div>
        <div
          class="flex-1 h-1 bg-gradient-to-r from-blue-500 dark:from-blue-800 to-gray-500 dark:to-gray-800"
        ></div>
        <div class="h-12 w-12 rounded-full bg-gray-500 dark:bg-gray-800"></div>
      </div>
    </section>
  </main>
</template>

<script setup lang="ts">
import { tabs } from "@/data/index";

useHead({
  title: "Jira software",
});
definePageMeta({
  layout: "default",
});
</script>
