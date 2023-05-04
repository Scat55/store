<template>
  <div class="cardItem">
    <img :src="require('../assets/image/cardItems/' + product_data.image)" alt="cardItem" />
    <p class="cardItem__price">{{ product_data.price }} руб</p>
    <div class="cardItem__brand">
      Бренд
      <span class="cardItem__brand-name">{{ product_data.brand }}</span>
    </div>
    <p class="cardItem__name">{{ product_data.name }}</p>
    <div class="cardItem__btns">
      <button class="cardItem__btn" @click="clickedBtn">Купить <span v-if="counter > 0">{{ counter }}</span></button>
      <button class="cardItem__btn" @click="clickedBtnOut" :disabled="isButtonDisabled">Отмена</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardItem",
  data() {
    return {
      counter: 0,
      isButtonDisabled: false,
    };
  },
  props: {
    product_data: {
      type: Object,
      default() {
        return {};
      },
    },
  },
  emits: ['counter'],
  methods: {
    clickedBtn() {
      this.counter++;
      this.$emit('counter')
    },
    clickedBtnOut() {
      if (this.counter === 0) {
        this.isButtonDisabled = !this.isButtonDisabled;
        this.isButtonDisabled = !this.isButtonDisabled;
      } else {
        this.counter--;
      }
    }
  }
};
</script>

<style lang="scss">
@import "../assets/styles/styles.scss";

.cardItem {
  display: flex;
  flex-direction: column;
  width: 300px;
  height: 390px;
  cursor: pointer;
  transition: all 0.3s;

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

  &__btns {
    display: flex;
    gap: 20px;
  }

  &__btn {
    background-color: #354153;
    color: #fff;
    border: none;
    border-radius: 18px;
    outline: none;
    padding: 15px;
    // width: 40%;
    margin-top: 10px;
    cursor: pointer;

    &:active {
      background-color: darken(#354153, 10%);
    }
  }
}
</style>