<script lang="ts" setup>
const props = defineProps({
  ctaIcon: {
    type: String,
    default: "house",
  },
});
</script>

<template><font-awesome-icon :icon="['fas', ctaIcon]" /></template>

<style lang="scss" scoped></style>
