<script setup lang="ts">
const { data: page } = await useAsyncData('app', () => queryContent('/').findOne())

useHead({
  meta: [
    { name: 'viewport', content: 'width=device-width, initial-scale=1' },
  ],
  link: [
    { rel: 'icon', href: 'https://failfast.blob.core.windows.net/upload/Logo_Varobol.png' }
  ],
  htmlAttrs: {
    lang: 'en'
  }
})

useSeoMeta({
  title: page.value.title,
  ogTitle: page.value.title,
  description: page.value.description,
  ogImage: page.value.imagelogo,
  ogImageWidth: "1024px",
  ogImageHeight: "640px",
  ogDescription: page.value.description + "app"
})
</script>

<template>

  <AppHeader />

  <UMain>
    <NuxtPage />
  </UMain>

  <AppFooter />

  <UNotifications />
</template>
