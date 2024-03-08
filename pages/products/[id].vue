<template>
  <div>
    <NuxtLink to="/">home</NuxtLink>
    <NuxtLink to="/about">about</NuxtLink>
    <NuxtLink to="/products">products</NuxtLink>
    <p>
      ProducT {{ route.params.id }} page
    </p>
  </div>
</template>

<script setup lang="ts">
const route = useRoute()

definePageMeta({
  validate: async (route) => {
    // Check if the id is made up of digits
    return typeof route.params.id === 'string' && /^\d+$/.test(route.params.id)
  }
})

// When accessing /posts/1, route.params.id will be 1

</script>