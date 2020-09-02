<template>
  <div class="select-wrapper">
    <select class="select">
      <option value="option" v-for="option in options">{{ option }}</option>
    </select>
    <img class="select-arrow" src="./chevron.svg" />
  </div>
</template>

<script>
export default {
  name: "AppSelect",
  props: {
    options: Array,
  },
};
</script>

<style lang="scss">
@import "select";
</style>
