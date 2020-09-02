<i18n src="./locales/lang.json"></i18n>

<template>
  <div class="home">
    <!--  section 1-->
    <section class="explore section_width">
      <div class="explore-wrapper">
        <div class="explore-wrapper-content">
          <h1>{{ $t("section_1.h1") }}</h1>
          <h3>{{ $t("section_1.h3") }}</h3>
          <div class="line" />
          <div class="selects">
            <app-select
              v-for="(options, index) in $t('section_1.options')"
              :options="[options]"
              :key="index"
            />
          </div>
          <app-button>{{ $t("section_1.btn") }}</app-button>
        </div>
        <div class="explore-wrapper-image">
          <img
            src="../../assets/images/Home/section_1_img.png"
            alt="img"
            class="img-fluid"
          />
        </div>
      </div>
    </section>
    <!--  END section 1-->

    <!--  section 2-->
    <section class="new-way section_width">
      <div class="new-way-wrapper">
        <div class="new-way-wrapper-image">
          <img
            src="../../assets/images/Home/section_2_img.png"
            alt="img"
            class="img-fluid"
          />
        </div>
        <div class="new-way-wrapper-content">
          <h2>{{ $t("section_2.h2") }}</h2>
          <p>{{ $t("section_2.text") }}</p>
          <app-button>{{ $t("section_2.btn") }}</app-button>
        </div>
      </div>
    </section>
    <!-- END section 2-->

    <!--  section 3-->
    <section class="destinations section_width">
      <div class="destinations-text">
        <h2>{{ $t("section_3.h2") }}</h2>
        <a href="#">{{ $t("section_3.a") }} &nbsp;></a>
      </div>
      <div class="images">
        <img
          :src="imgPath(img)"
          alt="img"
          v-for="img in $t('section_3.images')"
        />
      </div>
    </section>
    <!-- END section 3-->

    <!--  section 4-->
    <section class="guides section_width">
      <div class="guides-wrapper">
        <div class="guides-wrapper-content">
          <h2>{{ $t("section_4.h2") }}</h2>
          <p>{{ $t("section_4.text") }}</p>
          <app-button>{{ $t("section_4.btn") }}</app-button>
        </div>
        <div class="guides-wrapper-image">
          <img
            src="../../assets/images/Home/guides_1.png"
            alt="img"
            class="img-fluid"
          />
        </div>
      </div>
    </section>
    <!-- END section 4-->

    <!--  section 5-->
    <section class="testimonials section_width">
      <h2>{{ $t("section_5.h2") }}</h2>
      <div class="testimonials-wrapper">
        <div class="testimonials-wrapper-content">
          <div class="stars">
            <img
              src="../../assets/images/Home/star.png"
              alt="s"
              v-for="i in 5"
              :key="i"
              class="star"
            />
          </div>
          <p>{{ $t("section_5.text") }}</p>
          <h3>{{ $t("section_5.name") }}</h3>
          <h4>{{ $t("section_5.position") }}</h4>
        </div>
        <slider>
          <img
            src="../../assets/images/Home/slider_img.png"
            alt=""
            class="image"
          />
          <img
            src="../../assets/images/Home/destinations_1.png"
            alt=""
            class="image"
          />
        </slider>
      </div>
    </section>
    <!-- END section 5-->

    <!--  section 6-->
    <section class="trending section_width">
      <div class="trending-text">
        <h2>{{ $t("section_6.h2") }}</h2>
        <a href="#">{{ $t("section_6.a") }} &nbsp;></a>
      </div>
      <div class="cards">
        <div class="card" v-for="card in $t('section_6.cards')">
          <div class="card-main">
            <img :src="imgPath(card.img)" alt="" />
            <h3>{{ card.h3 }}</h3>
            <p>{{ card.text }}</p>
          </div>
          <a href="#">{{ card.a }}</a>
        </div>
      </div>
    </section>
    <!-- END section 6-->
  </div>
</template>

<script>
import AppSelect from "../../components/Select/AppSelect";
import AppButton from "../../components/Button/AppButton";
import Slider from "../../components/Slider/Slider";

export default {
  name: "Home",
  components: {
    AppSelect,
    AppButton,
    Slider,
  },
  methods: {
    imgPath(img) {
      return require(`../../assets/images/Home/${img}.png`);
    },
  },
};
</script>

<style lang="scss">
@import "home";
</style>
