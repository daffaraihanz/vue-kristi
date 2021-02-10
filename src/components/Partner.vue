<template>
  <div class="partner-logo">
    <div class="container">
      <carousel
        class="logo-carousel"
        :dots="false"
        :nav="false"
        :autoplay="true"
        :items="5"
        :autolay="true"
        :autoplayTimeout="1500"
        :loop="true"
        :autoplaySpeed="true"
      >
        <div class="logo-item" v-for="myPartner in partner" v-bind:key="myPartner.id">
          <div class="tablecell-inner">
            <img :src="myPartner.image" alt />
          </div>
        </div>
      </carousel>
    </div>
  </div>
</template>

<script>
import carousel from "vue-owl-carousel";

export default {
  name: "Partner",
  data: function() {
    return {
      partner: [
        {
          id: 1,
          image: "img/logo-carousel/logo-1.png"
        },
        {
          id: 2,
          image: "img/logo-carousel/logo-2.png"
        },
        {
          id: 3,
          image: "img/logo-carousel/logo-3.png"
        },
        {
          id: 4,
          image: "img/logo-carousel/logo-4.png"
        },
        {
          id: 4,
          image: "img/logo-carousel/logo-5.png"
        }
      ]
    };
  },
  components: {
    carousel
  }
};
</script>

<style scoped>
</style>