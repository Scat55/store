<template>
  <div class="modal">
    <div class="modal__item">
      <div class="modal__btn">
        <button class="modal__close">
          <img src="../assets/image/close-btn.svg" alt="closeBtn" @click="close">
        </button>
      </div>
      <div class=" modal__text">
        <h3 class="modal__title">Регистрация</h3>
        <p class="modal__subtitle">Введите логин и пароль в форме ниже</p>
      </div>
      <form class="modal__form">
        <label>Имя пользователя</label>
        <input type="text" class="modal__form-name" placeholder="Введите имя пользователя">
        <label class="modal__pas">Пароль</label>
        <input type="password" class="modal__form-password" placeholder="Введите пароль">
        <a href="#" class="form__link"><b>Восстановить пароль</b></a>
      </form>
      <p class="modal__registration">Есть аккаунт? <a href="#" class="registration__link"><b>Войти</b></a>
      </p>
      <div class="btn__come"><button class="modal__come">Зарегистрироваться</button></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "v-Modal",
  data() {
    return {

    }
  },
  emits: ['close'],
  methods: {
    close() {
      this.$emit('close')
    }
  }
}
</script>

<style lang="scss" scoped>
.modal {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: rgba(13, 20, 33, .4);
  // .modal__item

  &__item {
    width: 510px;
    height: 612px;
    background-color: #fff;
    border-radius: 16px;
  }

  &__btn {
    display: flex;
    justify-content: flex-end;
    align-items: center;
  }

  // .modal__close

  &__close {
    background: transparent;
    border: none;
    outline: none;
    cursor: pointer;
    margin: 16px 16px 0 0;
    padding-bottom: 32px;
  }

  // .modal__text

  &__text {
    border-top: 1px solid #EAECF0;
    text-align: center;

  }

  // .modal__title

  &__title {
    font-weight: 600;
    font-size: 32px;
    line-height: 40px;
    padding-top: 40px;
  }

  // .modal__subtitle

  &__subtitle {
    font-weight: 400;
    font-size: 18px;
    line-height: 28px;
    color: $greyColor;
    margin-bottom: 24px;
  }

  // .modal__form

  &__form {
    display: flex;
    flex-direction: column;
    margin: 0 83px;
  }

  label {
    font-weight: 500;
    font-size: 14px;
    line-height: 20px;
    color: $darkBlue;
  }

  // .modal__form-name

  &__form-name {
    height: 44px;
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    border: 1px solid #EAECF0;
    color: $greyColor;
    border-radius: 8px;
    outline: none;
    padding: 10px;

    &::placeholder {
      color: $greyColor;
    }
  }


  .modal__pas {
    margin-top: 16px;
  }

  // .modal__form-password

  &__form-password {
    height: 44px;
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    border: 1px solid #EAECF0;
    color: $greyColor;
    border-radius: 8px;
    outline: none;
    padding: 10px;

    &::placeholder {
      color: $greyColor;
    }
  }

  // .modal__registration

  &__registration {
    margin-top: 24px;
    text-align: center;
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    color: $greyColor;

  }

  // .modal__come

  &__come {
    width: 100%;
    margin: 0 24px;
    height: 44px;
    text-align: center;
    margin-top: 90px;
    font-weight: 600;
    font-size: 16px;
    line-height: 24px;
    background: #0D1421;
    border-radius: 8px;
    color: #fff;
    outline: none;
    cursor: pointer;
  }
}

.btn__come {
  display: flex;
  justify-content: center;
  align-items: center;
}

.form {

  // .form__link

  &__link {
    font-weight: 600;
    font-size: 16px;
    line-height: 24px;
    margin-top: 16px;
    text-decoration: none;
    color: #0D1421;
  }
}

.registration {

  // .registration__link

  &__link {
    font-weight: 600;
    font-size: 16px;
    line-height: 24px;
    margin-top: 16px;
    text-decoration: none;
    color: #0D1421;
  }
}
</style>