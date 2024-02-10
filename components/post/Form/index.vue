<template>
  <div class="modal-wrapper">
    <PostFormModal />
  </div>
</template>

<style lang="scss" scoped>
.modal-wrapper {
  position: absolute;
  top: 0;
  left: 0;

  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  background-color: rgba(0, 0, 0, 0.8);
  -webkit-backdrop-filter: blur(50px);
}
</style>
