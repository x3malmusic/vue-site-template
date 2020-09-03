<i18n src="./locales/lang.json"></i18n>

<template>
  <footer>
    <div class="footer section_width">
      <div class="footer-wrapper">
        <div class="footer-wrapper-block_1">
          <logo />
          <p class="footer-wrapper-block_1-text">{{ $t("block_1.text") }}</p>
          <p>{{ $t("block_1.copyright") }}</p>
        </div>
        <div class="footer-wrapper-lists">
          <ul v-for="list in $t('lists')" class="footer-wrapper-list">
            <li>
              <h3>{{ list.name }}</h3>
            </li>
            <li v-for="link in list.links">
              <a href="#">
                <p>{{ link }}</p>
              </a>
            </li>
          </ul>
        </div>
      </div>
      <hr />
    </div>
    <div class="socials">
      <img
        :src="imgPath(img)"
        alt=""
        v-for="img in $t('socials')"
        class="icon"
      />
    </div>
  </footer>
</template>

<script>
import Logo from "../Logo/Logo";

export default {
  name: "AppFooter",
  components: {
    Logo,
  },
  methods: {
    imgPath(img) {
      return require(`../../assets/images/Socials/${img}.png`);
    },
  },
};
</script>

<style lang="scss">
@import "app-footer";
</style>
