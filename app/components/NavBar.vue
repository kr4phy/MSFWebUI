<script setup lang="ts">
import type { NavigationMenuItem } from '@nuxt/ui'

const route = useRoute()

const items = computed<NavigationMenuItem[]>(() => [
  {
    label: 'Home',
    to: '/',
    active: route.path === '/'
  },
  {
    label: 'Modules',
    to: '/modules',
    active: route.path.startsWith('/modules')
  },
  {
    label: 'Settings',
    to: '/settings',
    active: route.path.startsWith('/settings')
  }
])
</script>

<template>
  <UHeader>
    <template #left>
      <NuxtLink to="/" class="focus-visible:outline-3 outline-primary/25 rounded-md p-1 -ms-1">
        <AppLogo class="w-auto h-6 shrink-0" />
      </NuxtLink>
      <UNavigationMenu :items="items" class="ms-4" />
    </template>

    <template #right>
      <UColorModeButton />

      <UButton to="https://github.com/kr4phy/MSFWebUI" target="_blank" icon="i-simple-icons-github" aria-label="GitHub" color="neutral" variant="ghost" />
    </template>
  </UHeader>
</template>
