<template>
  <a
    :class="{ fullWidth: fullWidth }"
    :style="{ background: background, color: color }"
    class="button"
    >{{ title }}</a
  >
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default() {
        return "Click here";
      },
    },
    background: {
      type: String,
      default() {
        return "#eee";
      },
    },
    color: {
      type: String,
      default() {
        return "#000";
      },
    },
    link: {
      type: String,
      default() {
        return "/";
      },
    },
    fullWidth: {
      type: Boolean,
      default() {
        return false;
      },
    },
  },
};
</script>

<style scoped>
.button {
  border: none;
  outline: none;
  margin: 0.5rem;
  font-size: 1.2rem;
  font-weight: bold;
  padding: 0.5rem;
  border-radius: 10px;
  text-decoration: none;
}
.button:hover {
  cursor: pointer;
  filter: brightness(95%);
}
.fullWidth {
  display: block;
  width: 100%;
}
</style>
