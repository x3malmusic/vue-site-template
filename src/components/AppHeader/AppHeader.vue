<i18n src="./locales/lang.json"></i18n>

<template>
  <nav class="navbar">
    <logo />
    <div class="menu-collapsible" :class="collapse && 'menu-active'">
      <ul class="nav-links">
        <li class="nav-link" v-for="link in $t('navLinks')">
          <router-link :to="link.path">
            {{ link.name }}
          </router-link>
        </li>
      </ul>
      <app-button type="btn-bordered">{{ $t("btnLogin") }}</app-button>
      <app-button>{{ $t("btnRegister") }}</app-button>
    </div>
    <burger-button :collapse="collapse" @click="menuCollapse" />
  </nav>
</template>

<script>
import AppButton from "../Button/AppButton";
import BurgerButton from "../BurgerButton/BurgerButton";
import Logo from "../Logo/Logo";

export default {
  name: "AppHeader",
  components: {
    AppButton,
    BurgerButton,
    Logo,
  },
  data: () => ({
    collapse: false,
  }),
  methods: {
    menuCollapse() {
      this.collapse = !this.collapse;
    },
  },
};
</script>

<style lang="scss">
@import "app-header";
</style>
