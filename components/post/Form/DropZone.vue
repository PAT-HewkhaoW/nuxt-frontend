<script lang="ts" setup>
import { PhotoIcon } from "@heroicons/vue/24/outline";
const active = ref(false);

const toggleActive = () => {
  active.value = true;
  setTimeout(() => {
    active.value = false;
  }, 1000); // 1000 milliseconds = 1 second
};
</script>

<template>
  <div class="drop-zone">
    <input type="file" id="file-dropzone" @click="toggleActive" />
    <label for="file-dropzone">
      <!-- <PhotoIcon color="var(--color-text)" /> -->
      <font-awesome-icon
        icon="fa-solid fa-image "
        size="lg"
        :bounce="active"
        :style="{ color: 'var(--color-text)' }"
      />
      <p class="inconsolata">Choose Image</p>
    </label>
  </div>
</template>

<style lang="scss" scoped>
.drop-zone {
  width: 100%;
  border: 2px dashed var(--color-text);
  border-radius: 6px;
  display: grid;
  place-items: center;

  input[type="file"] {
    width: 0;
    height: 0;
    z-index: -1;
    position: relative;
    overflow: hidden;
    opacity: hidden;
  }

  label {
    width: 100%;
    height: 100%;
    padding: 24px 0;

    display: flex;
    justify-content: center;
    gap: 8px;
    font-awesome-icon {
      color: var(--color-text);
    }
  }
}
</style>
