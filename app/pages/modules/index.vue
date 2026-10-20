<script setup lang="ts">
const tabItems = [
  {
    label: 'Auxiliary',
    icon: 'i-lucide-tool',
    slot: 'auxiliary'
  },
  {
    label: 'Encoder',
    icon: 'i-lucide-code',
    slot: 'encoder'
  },
  {
    label: 'Evasion',
    icon: 'i-lucide-shield',
    slot: 'evasion'
  },
  {
    label: 'Exploit',
    icon: 'i-lucide-bomb',
    slot: 'exploit'
  },
  {
    label: 'NOP',
    icon: 'i-lucide-circle',
    slot: 'nop'
  },
  {
    label: 'Payload',
    icon: 'i-lucide-package',
    slot: 'payload'
  },
  {
    label: 'Post',
    icon: 'i-lucide-clipboard',
    slot: 'post'
  }
]
</script>

<template>
  <UPage>
    <template #left>
      <UPageAside>
        <p>sidebar</p>
      </UPageAside>
    </template>

    <UTabs :items="tabItems" class="py-4">
      <template #auxiliary>
        <p>TODO: {{ "<Auxiliary />" }} tag</p>
      </template>
      <template #encoder>
        <p>TODO: {{ "<Encoder />" }} tag</p>
      </template>
      <template #evasion>
        <p>TODO: {{ "<Evasion />" }} tag</p>
      </template>
      <template #exploit>
        <p>TODO: {{ "<Exploit />" }} tag</p>
      </template>
      <template #nop>
        <p>TODO: {{ "<NOP />" }} tag</p>
      </template>
      <template #payload>
        <p>TODO: {{ "<Payload />" }} tag</p>
      </template>
      <template #post>
        <p>TODO: {{ "<Post />" }} tag</p>
      </template>
    </UTabs>

    <template #right />
  </UPage>
</template>
