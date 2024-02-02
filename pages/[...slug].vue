<template>
  <main>
    <ContentDoc />
    {{ data.body }}
  </main>
</template>
<script setup lang="ts">
  const { data } = await useAsyncData('home', () => queryContent('data').findOne())
</script>
