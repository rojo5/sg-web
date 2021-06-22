<template>
  <VueSlickCarousel v-bind="slickOptions">
    <div v-for="i in 4" :key="i" class="img-wrapper">
      <img :src="`./carousel/${i}.jpg`" />
    </div>
  </VueSlickCarousel>
</template>

<script>
export default {
  name: "carousel",
  data() {
    return {
      slickOptions: {
        slidesToShow: 1,
        arrows: false,
        infinite: true,
        fade: true,
        autoplay: true,
        speed: 5000,
        autoplaySpeed: 5000,
      },
    };
  },
};
</script>

<style lang="scss" scoped>
.img-wrapper img {
  margin: auto;
  width: 100%;
  height: 100%;
  padding: 0;
  background-image: linear-gradient(gray 100%, transparent 0);
}
</style>