<template>
  <div id="container">
    <Header />
    <router-view />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/header.vue";
import Footer from "./components/footer.vue";

export default {
  components: {
    Header,
    Footer,
  },
};
</script>

<style>
#container {
  width: 100%;
  height: 100%;
}
</style>
