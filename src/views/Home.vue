<template>
  <section class="home">
    <Header />
    <Hero />
    <Catalog />
    <Gallery />
    <Partner />
    <Footer />
  </section>
</template>

<script>
import Header from "../components/Header";
import Hero from "../components/Hero";
import Catalog from "../components/Catalog";
import Gallery from "../components/Gallery";
import Partner from "../components/Partner";
import Footer from "../components/Footer";

export default {
  name: "Home",
  components: {
    Header,
    Hero,
    Catalog,
    Gallery,
    Partner,
    Footer
  }
};
</script>

<style scoped>
</style>
