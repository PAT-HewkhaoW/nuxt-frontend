<script lang="ts"></script>

<template>
  <div class="left-sidebar">
    <div class="brand-container">
      <icons iconHeight="36" fill-color="#181818" />
    </div>
    <div class="nav-link">
      <sidebarLeftTab>
        <template v-slot:icon>icon</template>
        <template v-slot:name>name</template>
      </sidebarLeftTab>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.left-sidebar {
  position: relative;

  height: 100vh;

  .brand-container {
    max-width: fit-content;
  }
}
</style>
