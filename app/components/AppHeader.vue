<script setup lang="ts">
const nuxtApp = useNuxtApp()
const { activeHeadings, updateHeadings } = useScrollspy()

const links = computed(() => [{
  label: 'Features',
  to: '#features',
  icon: 'i-heroicons-cube-transparent',
  active: activeHeadings.value.includes('features') && !activeHeadings.value.includes('pricing')
}, {
  label: 'Pricing',
  to: '#pricing',
  icon: 'i-heroicons-credit-card',
  active: activeHeadings.value.includes('pricing') && !activeHeadings.value.includes('testimonials')
}, {
  label: 'Testimonials',
  to: '#testimonials',
  icon: 'i-heroicons-academic-cap',
  active: activeHeadings.value.includes('testimonials')
}, {
  label: 'FAQ',
  to: '#faq',
  icon: 'i-heroicons-question-mark-circle',
  active: activeHeadings.value.includes('faq')
}])

nuxtApp.hooks.hookOnce('page:finish', () => {
  updateHeadings([
    document.querySelector('#features'),
    document.querySelector('#pricing'),
    document.querySelector('#testimonials'),
    document.querySelector('#faq')
  ])
})
</script>

<template>
  <UHeader>
    <template #logo>
      <UAvatar class="dark:bg-white" size="sm" src="https://failfast.blob.core.windows.net/upload/Logo_Varobol.png" />
      <label class="text-[#035ea5] dark:text-white">VAROBOL</label>
    </template>

    <template #panel>
      <UAsideLinks :links="links" />
      <UDivider class="my-6" />
    </template>
  </UHeader>
</template>
