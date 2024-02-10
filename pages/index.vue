<template>
  <div>
    this is index page

    <pre>
      <NuxtLink to="/feed">feed</NuxtLink>
      <NuxtLink to="/signup">signin</NuxtLink>
      <NuxtLink to="/signin">signup</NuxtLink>
    </pre>
  </div>
</template>

<script lang="ts" setup>
definePageMeta({
  layout: "default",
});
</script>

<style></style>
