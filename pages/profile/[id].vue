<script setup>
const route = useRoute();
</script>

<template>
  <NuxtLayout>
    <div>this is profile of user id : {{ route.params.id }}</div>
  </NuxtLayout>
</template>
