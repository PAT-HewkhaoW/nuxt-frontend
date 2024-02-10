<template>
  <div class="post-container">
    <div class="post-modal">
      <div class="modal-top">
        <div class="close-btn" @click="">
          <font-awesome-icon
            icon="fa-solid fa-xmark"
            style="color: var(--color-text)"
          />
        </div>
        <div class="modal-title">
          <p class="inconsolata">Add new post</p>
        </div>
      </div>
      <div class="modal-content">
        <div class="post-form">
          <PostFormContentInput />
        </div>
        <div class="post-attachment">
          <div class="cta-contianer">
            <font-awesome-icon icon="fa-solid fa-image" />
            <font-awesome-icon icon="fa-solid fa-location-dot" />
            <font-awesome-icon icon="fa-solid fa-share-nodes" />
            <font-awesome-icon icon="fa-solid fa-location-dot" />
          </div>
          <PostFormDropZone />
          <PostFormAttachment />
        </div>
      </div>
      <div class="modal-cta">
        <UiButton class="rounded fill" @on-click="">
          <div>post</div>
        </UiButton>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import "../../../assets/base.scss";
.post-container {
  width: 100%;
  max-width: $breakpoint-sm;

  .post-modal {
    padding: 24px;
    width: 100%;

    background-color: var(--color-bg);
    border: 1px solid var(--color-heading);
    border-radius: 16px;
    .modal-top {
      display: flex;
      justify-content: space-between;
      width: 100%;
      color: var(--color-text);
      .close-btn {
      }

      .modal-title {
      }
    }

    .modal-content {
    }

    .modal-cta {
    }
  }
}
</style>
