<template>
  <div>
    <NuxtLink to="/">home</NuxtLink>
    <NuxtLink to="/about">about</NuxtLink>
    <NuxtLink to="/products">products</NuxtLink>
    main page
  </div>
  <div>
    {{ users }}
  </div>
</template>

<script setup lang="ts">
const description = ref('My amazing site.')

useHead({
  meta: [
    { name: 'description', content: description }
  ],
})

const { data: users } = await useFetch('/api/test')

</script>