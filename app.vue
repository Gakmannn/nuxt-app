<template>
  <div>
    <MyComponent />
    <NuxtPage />
    {{ appConfig }}
  </div>
</template>

<script setup lang="ts">
useSeoMeta({
  title: 'Meet Nuxt',
  description: 'The Intuitive Vue Framework.'
})
const appConfig = useAppConfig()
</script>