<template>
  <section class="hero-section">
    <carousel
      class="hero-items"
      :items="1"
      :nav="false"
      :autoplay="true"
      :autoplayTimeout="4000"
      :autoplaySpeed="1000"
    >
      <div
        class="single-hero-items set-bg"
        v-for="myCarousel in carousel"
        v-bind:key="myCarousel.id"
        :style="{ backgroundImage: `url(${myCarousel.bg})` }"
      >
        <div class="container">
          <div class="row">
            <div class="col-lg-5 lala">
              <span>{{ myCarousel.kategori }}</span>
              <h1>{{ myCarousel.title }}</h1>
              <p>{{ myCarousel.desc }}</p>
              <a href="#" class="primary-btn">Shop Now</a>
            </div>
          </div>
        </div>
      </div>
    </carousel>
  </section>
</template>

<script>
// dependencies
import carousel from "vue-owl-carousel";

export default {
  name: "Hero",
  props: ["myCarousel"],
  components: {
    carousel
  },
  data: function() {
    return {
      carousel: [
        {
          id: 1,
          kategori: "ADULT,SWEETER",
          title: "Violet Sweet",
          desc:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore",
          bg: "img/hero-1.jpg"
        },
        {
          id: 2,
          kategori: "KID,JACKET",
          title: "Yellow IT",
          desc:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore",
          bg: "img/hero-2.jpg"
        }
      ]
    };
  }
};
</script>

<style scoped>
.lala {
  text-align: left;
}
</style>