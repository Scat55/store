<template>
  <div class="cardItem">
    <img
      :src="require('../assets/image/cardItems/' + product_data.image)"
      alt="cardItem"
    />
    <p class="cardItem__price">{{ product_data.price }} руб</p>
    <div class="cardItem__brand">
      Бренд
      <span class="cardItem__brand-name">{{ product_data.brand }}</span>
    </div>
    <p class="cardItem__name">{{ product_data.name }}</p>
  </div>
</template>

<script>
export default {
  name: "CardItem",
  data() {
    return {};
  },
  props: {
    product_data: {
      type: Object,
      default() {
        return {};
      },
    },
  },
};
</script>

<style lang="scss">
@import "../assets/styles/styles.scss";
.cardItem {
  width: 300px;
  height: 390px;
  cursor: pointer;
  transition: all 0.3s;

  &:hover {
    transform: scale(1.03);
  }
  img {
    width: 270px;
  }

  &__price {
    font-weight: 500;
    font-size: 18px;
    line-height: 28px;
    color: #0d1421;
  }
  &__brand {
    font-weight: 500;
    font-size: 14px;
    line-height: 20px;
    color: #667085;

    &-name {
      font-weight: 500;
      font-size: 14px;
      line-height: 20px;
      color: #354153;
    }
  }

  &__name {
    font-weight: 400;
    font-size: 12px;
    line-height: 20px;
    color: #667085;
  }
}
</style>