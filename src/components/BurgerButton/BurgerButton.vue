<template>
  <button
    :class="collapse ? 'burger-btn change' : 'burger-btn'"
    @click="$emit('click')"
  >
    <div class="bar1" />
    <div class="bar2" />
    <div class="bar3" />
  </button>
</template>

<script>
export default {
  name: "BurgerButton",
  props: {
    collapse: Boolean,
  },
};
</script>

<style lang="scss">
@import "burger-button";
</style>
