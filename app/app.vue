<script setup lang="ts">
useHead({
  meta: [
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
  link: [
    { rel: 'icon', href: '/favicon.ico' }
  ],
  htmlAttrs: {
    lang: 'en'
  }
})

const title = 'MSFWebUI'
const description = 'Web frontend for Metasploit Framework'

useSeoMeta({
  title,
  description,
  ogTitle: title,
  ogDescription: description,
  ogImage: '',
  twitterCard: 'summary_large_image'
})
</script>

<template>
  <UApp>
    <NavBar />

    <UMain>
      <NuxtPage />
    </UMain>

    <USeparator icon="i-simple-icons-nuxtdotjs" />

    <UFooter>
      <template #left>
        <p class="text-sm text-muted">
          Built with Nuxt UI • © {{ new Date().getFullYear() }}. kr4phy All rights reserved.
        </p>
      </template>

      <template #right>
        <UButton
          to="https://github.com/kr4phy/MSFWebUI"
          target="_blank"
          icon="i-simple-icons-github"
          aria-label="GitHub"
          color="neutral"
          variant="ghost"
        />
      </template>
    </UFooter>
  </UApp>
</template>
