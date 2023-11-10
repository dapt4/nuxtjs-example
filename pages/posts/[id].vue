<script setup>
  const route = useRoute()
  const { data: post } = useFetch(`https://jsonplaceholder.typicode.com/posts/${route.params.id}`)
</script>

<template>
  <div v-if="post">
    <h1 class="text-3xl  font-bold">{{ post.title }}</h1>
    <p class="mt-3">{{ post.body }}</p>
  </div>
</template>

<style scoped>
/* code... */
</style>
