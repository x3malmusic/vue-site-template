<template>
  <div id="app">
    <locale-changer />
    <app-header />
    <transition name="fade" mode="out-in">
      <router-view />
    </transition>
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
