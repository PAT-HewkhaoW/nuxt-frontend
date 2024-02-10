<template>
  <textarea
    onkeydown="if(event.keyCode===9){var v=this.value,s=this.selectionStart,e=this.selectionEnd;this.value=v.substring(0, s)+'\t'+v.substring(e);this.selectionStart=this.selectionEnd=s+1;return false;}"
    name="NewPostInput"
    id="NewPostInput"
    rows="30"
    placeholder="post something."
    wrap="soft"
  ></textarea>
</template>

<style lang="scss" scoped>
*,
*:focus {
  outline: none;
}
textarea {
  margin: 24px 0 0 0;
  padding: 12px;
  width: 100%;
  resize: none;

  border: 0;
  height: auto;

  &:focus {
  }
}
</style>
