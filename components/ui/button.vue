<script lang="ts" setup>
const emits = defineEmits(["onClick"]);

function handleClick(event: any) {
  emits("onClick", event);
}
</script>

<template>
  <button class="ui-button inconsolata" @click="handleClick">
    <slot />
  </button>
</template>

<style lang="scss" scoped>
.ui-button {
  display: flex;
  justify-content: center;
  align-items: center;
  width: fit-content;

  font-size: 15px;
  font-weight: 700;
  letter-spacing: 0.075rem;
  padding: 10px 18px;
  color: var(--color-white);

  border: 0px solid;
  border-radius: 6px;

  background-color: var(--color-heading);

  transition: 0.2s ease;

  &:hover {
    background-color: var(--color-black);
  }

  &:focus {
    background-color: var(--color-accent);
  }

  &.fill {
    width: 100%;
  }

  &.rounded {
    border-radius: 9999px;
  }
}
</style>
