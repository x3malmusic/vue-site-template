<template>
  <div id="app">
    <app-header />
    <router-view />
    <app-footer />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader/AppHeader";
import AppFooter from "./components/AppFooter/AppFooter";

export default {
  name: "App",
  components: {
    AppHeader,
    AppFooter,
  },
};
</script>
]

<style lang="scss"></style>
