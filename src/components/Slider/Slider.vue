<template>
  <div class="slider">
    <div class="slider-wrapper">
      <slot></slot>
    </div>
    <div class="slider-control">
      <button class="slider-control-btn-left" @click="showPrev">
        <img src="./chevron.svg" alt="left" class="arrow-left" />
      </button>
      <button class="slider-control-btn-right" @click="showNext">
        <img src="./chevron.svg" alt="right" class="arrow-right" />
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Slider",
  data: () => ({
    currentImg: 0,
    images: 0,
  }),
  methods: {
    showNext() {
      this.currentImg++;
      if (this.currentImg > this.images) this.currentImg = 0;
      this.showSlide();
    },

    showPrev() {
      this.currentImg--;
      if (this.currentImg < 0) this.currentImg = this.images;
      this.showSlide();
    },

    showSlide() {
      this.$slots.default.forEach((el, i) => {
        if (this.currentImg != i) el.elm.className += " imageHide";
        else
          el.elm.className = el.elm.className
            .split(" ")
            .filter((e) => e != "imageHide")
            .join(" ");
      });
    },
  },

  mounted() {
    this.images = this.$slots.default.length - 1;
    this.showSlide();
  },
};
</script>

<style lang="scss">
@import "slider";
</style>
