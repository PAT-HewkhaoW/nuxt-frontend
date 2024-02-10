<script lang="ts" setup>
const props = defineProps({
  active: {
    type: Boolean,
    default: false,
  },
  link: {
    type: String,
    default: "/",
  },
});

const isActive = computed(() => {
  props.active ? "tab-active" : "";
});
</script>

<template>
  <NuxtLayout :to="{ path: link }" :class="isActive">
    <div class="icon-container">
      <slot name="icon"></slot>
    </div>

    <div class="name-container">
      <slot name="name"></slot>
    </div>
  </NuxtLayout>
</template>

<style lang="scss" scoped>
.tab-active {
  background-color: rgb(var(--color-text), 0.8);
}
</style>
