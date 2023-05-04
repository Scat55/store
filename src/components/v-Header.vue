<template>
  <div class="header">
    <div class="container">
      <div class="wrapper">
        <div class="header__logo">
          <img src="../assets/image/Logo.svg" alt="logo" class="logo" />
          <a href="#" class="header__title">Курсовой макет </a>
        </div>
        <div class="header__buttons">
          <button class="header__btn">
            <img src="../assets/image/userIcon.svg" alt="person" @click="statusM" />
          </button>
          <button class=" header__btn">
            <img src="../assets/image/cartIcon.svg" alt="goToCart" />
          </button>
        </div>
      </div>
    </div>
  </div>
  <Modal v-if="status" @close="status = false" />
</template>

<script>
import Modal from "@/components/v-Modal.vue";
export default {

  name: "v-Header",
  data() {
    return {
      status: false
    };
  },
  emits: ['close', 'counter'],
  components: {
    Modal
  },

  methods: {
    statusM() {
      this.status = !this.status
    }
  }

};
</script>

<style lang="scss" >
@import "../assets/styles/styles.scss";

.wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.header {
  border-bottom: 1px solid #eaecf0;

  &__logo {
    display: flex;
    gap: 24px;
  }

  &__title {
    font-weight: 600;
    font-size: 24px;
    line-height: 32px;
    text-decoration: none;
    padding: 20px 0;
    color: $darkBlue;
  }

  &__buttons {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 21px;
  }

  &__btn {
    background-color: transparent;
    border: none;
    outline: none;
    cursor: pointer;
    transition: all 0.3s;

    &:hover {
      transform: scale(1.1);
    }
  }
}
</style>