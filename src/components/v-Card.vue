<template>
  <div class="crad">
    <div class="container">
      <buttonItem />
      <div class="card__list">
        <cardItem v-for="product in products" :key="product.article" :product_data="product" />
      </div>
    </div>
  </div>
</template>

<script>

import cardItem from "../components/v-CardItem";
import buttonItem from "../components/v-Button.vue";
import axios from 'axios';

export default {
  name: "v-Card",
  data() {
    return {
      products: [],
    };
  },
  components: {
    buttonItem,
    cardItem,
  },
  mounted() {
    axios.get('https://644e82564e86e9a4d8faaedc.mockapi.io/product_data')
      .then(response => {
        this.products = response.data;
      })
  }
};
</script>

<style lang="scss">
@import "../assets/styles/styles.scss";

.card {
  &__list {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 16px;
    gap: 10px;
  }
}
</style>