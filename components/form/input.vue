<script>
export default {
  props: {
    label: { type: String, default: "labels" },
    dataModel: {
      type: String,
      required: true,
    },
    type: { type: String, default: "text" },
    isRequired: {
      type: Boolean,
      default: false,
    },
  },

  data() {
    return {
      // labels: "input label",
    };
  },
};
</script>

<template>
  <div class="input-wrapper">
    <input
      placeholder=""
      :v-model="dataModel"
      :type="type"
      :required="isRequired"
    />
    <label class="inconsolata">{{ label }}</label>
  </div>
</template>

<style lang="scss" scoped>
*,
*:focus {
  outline: none;
}
.input-wrapper {
  width: 100%;
  position: relative;
  padding: 8px 0;

  input {
    padding: 0 16px;
    display: block;
    width: 100%;
    height: 36px;
    border: 1px solid var(--color-text);
    border-radius: 6px;
    background: transparent;

    transition: 0.3s ease;

    &:focus {
      border-color: var(--color-accent);

      + label {
        color: var(--color-accent);
      }
    }

    &:focus,
    &:not(:placeholder-shown) {
      + label {
        font-size: 11px;
        top: 3px;
        background-color: var(--color-bg);
      }
    }

    &:invalid {
      border-color: var(--color-danger);
      + label {
        color: var(--color-danger);
      }
    }
  }

  label {
    position: absolute;
    z-index: 2;
    top: 18px;
    left: 10px;
    padding: 0 8px;

    font-size: 14px;
    color: var(--color-text);
    text-transform: lowercase;
    cursor: text;
    pointer-events: none;
    transition: 0.1s ease;

    font-weight: 500;
  }
}
</style>
