<template>
  <section class="women-banner spad">
    <div class="container-fluid">
      <div class="row">
        <div class="col-lg-12 mt-5">
          <carousel
            class="product-slider"
            :nav="false"
            :dots="false"
            :autoplay="true"
            :autoplayHoverPause="true"
            :autoplayTimeout="2000"
            :responsive="{0:{items:1,nav:true},600:{items:2},850:{items:3},1199:{items:5}}"
          >
            <div class="product-item" v-for="myKatalog in katalog" v-bind:key="myKatalog.id">
              <div class="pi-pic">
                <img :src="myKatalog.image" alt />
                <ul>
                  <li class="w-icon active">
                    <router-link to="/product">
                      <i class="icon_bag_alt"></i>
                    </router-link>
                  </li>
                  <li class="quick-view">
                    <router-link to="/product">+ Quick View</router-link>
                  </li>
                  <li class="w-icon">
                    <router-link to="/product">
                      <i class="icon_bag_alt"></i>
                    </router-link>
                  </li>
                </ul>
              </div>
              <div class="pi-text">
                <div class="catagory-name">{{ myKatalog.category }}</div>
                <a href>
                  <h5>{{ myKatalog.title }}</h5>
                </a>
                <div class="product-price">{{ myKatalog.price }}</div>
              </div>
            </div>
          </carousel>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import carousel from "vue-owl-carousel";

export default {
  name: "catalog",
  components: {
    carousel
  },
  data: function() {
    return {
      katalog: [
        {
          id: 1,
          category: "TOWEL",
          title: "Autumn Sweater",
          price: "Rp 800.000",
          image: "img/products/women-1.jpg"
        },
        {
          id: 2,
          category: "SWEATER",
          title: "Young Red Sweater",
          price: "Rp 1.800.000",
          image: "img/products/women-2.jpg"
        },
        {
          id: 3,
          category: "SWEATER",
          title: "Sweety Grey",
          price: "Rp 200.000",
          image: "img/products/women-3.jpg"
        },
        {
          id: 4,
          category: "TOWEL",
          title: "Converse Shoes",
          price: "Rp 500.000",
          image: "img/products/women-4.jpg"
        },
        {
          id: 5,
          category: "TOWEL",
          title: "Autumn Sweater",
          price: "Rp 800.000",
          image: "img/products/women-1.jpg"
        },
        {
          id: 6,
          category: "SWEATER",
          title: "Young Red Sweater",
          price: "Rp 1.800.000",
          image: "img/products/women-2.jpg"
        },
        {
          id: 7,
          category: "SWEATER",
          title: "Sweety Grey",
          price: "Rp 200.000",
          image: "img/products/women-3.jpg"
        },
        {
          id: 8,
          category: "TOWEL",
          title: "Converse Shoes",
          price: "Rp 500.000",
          image: "img/products/women-4.jpg"
        }
      ]
    };
  }
};
</script>

<style scoped>
.product-item {
  margin: 0 10px;
}
</style>