<template>
  <div>
    <div class="left-side">
      <sidebarLeft />
    </div>
    <div class="feed-section">
      <slot />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.left-side {
  position: fixed;
  left: 0;
  top: 0;
}

.feed-section {
}
</style>
