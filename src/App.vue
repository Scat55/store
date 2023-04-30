<template>
  <div id="app">
    <Header />
    <Card />
    <Footer />
  </div>
</template>

<script>
import Header from "@/components/v-Header.vue";
import Card from "@/components/v-Card.vue";
import Footer from "@/components/v-Footer.vue";
export default {
  name: "App",
  components: {
    Header,
    Card,
    Footer,
  },
};
</script>

<style lang="scss">
@import "./assets/styles/styles";
* {
  font-family: $font;
}
#app {
}
</style>