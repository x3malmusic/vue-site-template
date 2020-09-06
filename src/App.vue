<template>
  <div id="app">
    <locale-changer />
    <app-header />
    <router-view />
    <app-footer />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader/AppHeader";
import AppFooter from "./components/AppFooter/AppFooter";
import LocaleChanger from "./components/LocaleChanger/LocaleChanger";

export default {
  name: "App",
  components: {
    AppHeader,
    AppFooter,
    LocaleChanger,
  },
};
</script>
]

<style lang="scss"></style>
