<template>
  <div class="header">
    <div class="container">
      <div class="wrapper">
        <div class="header__logo">
          <img src="../assets/image/Logo.svg" alt="logo" class="logo" />
          <a href="#" class="header__title">Курсовой макет</a>
        </div>
        <div class="header__buttons">
          <button class="header__btn">
            <img src="../assets/image/userIcon.svg" alt="person" />
          </button>
          <button class="header__btn">
            <img src="../assets/image/cartIcon.svg" alt="goToCart" />
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "v-Header",
  data() {
    return {};
  },
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