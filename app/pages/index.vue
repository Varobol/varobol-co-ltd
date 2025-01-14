<script setup lang="ts">
const { data: page } = await useAsyncData('index', () => queryContent('/').findOne())

useSeoMeta({
  title: page.value.title,
  ogTitle: page.value.title,
  description: page.value.description,
  // ogImage: page.value.imagelogo,
  ogImage: '/Logo_Varobol.png',
  ogImageWidth: "1024",
  ogImageHeight: "640",
  ogDescription: page.value.description + "index6"
})

</script>

<template>
  <UPage>
    <UPageBody :ui="{ wrapper: 'mt-0 pb-0' }">
      <ULandingSection class="bg-[#035ea5] " :ui="{ wrapper: 'sm:py-0 ' }">
        <UPageHero
          :ui="{ wrapper: 'py-0 sm:py-16 pt-0 sm:pt-0 ', container: 'sm:gap-y-0', title: 'lg:text-7xl  text-white dark:text-white', description: 'lg:text-3xl' }"
          description="" align="right">
          <template #title>
            <label class="text-5xl lg:text-7xl">The Future is Here</label>
          </template>
          <template #description>
            <p class="text-white :dark:text-white lg:text-3xl">Next Gen platform</p>
          </template>
          <img src="https://failfast.blob.core.windows.net/upload/webvarobol/session1.png"
            class="lg:h-3/4 dark:ring-gray-700 justify-self-center " />
        </UPageHero>
      </ULandingSection>

      <ULandingSection class="bg-[#f7f7f7]" :ui="{ wrapper: 'py-0 sm:py-0 md:py-0' }">
        <ULandingHero
          :ui="{ wrapper: 'py-0 sm:py-0 md:py-0 pt-16 sm:pt-16 md:pt-16', title: 'text-black dark:text-black', description: 'lg:text-3xl text-black dark:text-black' }"
          title="" description="Everything in your hand" orientation="vertical">
          <template #title>
            <label>Connect All in <label class="text-[#ed1c24]">One</label></label>
          </template>
          <template #default>
            <img src="https://failfast.blob.core.windows.net/upload/webvarobol/session2.png"
              class="w-full  ring-gray-300 dark:ring-gray-700" />
          </template>
        </ULandingHero>
      </ULandingSection>



      <ULandingSection class="bg-[#dae7f1]" :ui="{ wrapper: 'py-8 sm:py-0 ' }">
        <UPageHero :ui="{
          wrapper: 'py-0 sm:py-0  pt-0 sm:pt-0 ', container: 'sm:gap-y-0', title: 'lg:text-6xl text-black dark:text-black'
          , description: 'lg:text-3xl text-black dark:text-black'
        }" align="left">
          <template #title>
            <label class="text-5xl lg:text-7xl">Ultimate Security</label>
          </template>
          <template #description>
            <p class="lg:text-3xl">As Good as International Banks
            </p>
          </template>
          <img src="https://failfast.blob.core.windows.net/upload/webvarobol/session3.png"
            class="lg:h-3/4     dark:ring-gray-700 justify-self-center " />
        </UPageHero>
      </ULandingSection>



      <ULandingSection class="bg-[#f7f7f7]" :ui="{ wrapper: 'sm:py-0 py-0' }">
        <ULandingHero
          :ui="{ wrapper: 'py-0 sm:py-0 md:py-0 pt-16 sm:pt-16 md:pt-16', title: 'text-black dark:text-black', description: 'lg:text-3xl text-black dark:text-black' }"
          title="Make Lives Happier" description="Digital Transformation With Ease" orientation="vertical">
          <template #default>
            <img class="-mt-[96px]" src="https://failfast.blob.core.windows.net/upload/webvarobol/session4.png">
          </template>
        </ULandingHero>
      </ULandingSection>

      <ULandingSection class="bg-[#dae7f1]" :ui="{ wrapper: 'py-8 sm:py-0 lg:py-8 pt-0 sm:pt-0 lg:pt-8' }">
        <UPageHero
          :ui="{ wrapper: 'py-0 sm:py-0  pt-16 sm:pt-16 md:pt-16', title: 'text-black dark:text-black', description: 'text-black dark:text-black' }"
          title="" description="" orientation="vertical">
          <template #title>
            <label class="text-5xl lg:text-7xl">Vitsit Mana website</label>
          </template>
          <template #description>
            <p class="lg:text-3xl mb-4">Learn more about Mana platform</p>
            <UButton size="lg"
              class="bg-[#035ea5] dark:bg-[#035ea5] dark:text-white dark:hover:bg-[#3e91d1] hover:bg-[#3e91d1]"
              to="https://mana2018.co.th" target="_blank">Open
              Mana Web</UButton>
          </template>
        </UPageHero>
      </ULandingSection>
    </UPageBody>
  </UPage>
</template>
