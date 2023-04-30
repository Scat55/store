<template>
  <div class="footer">
    <div class="container">
      <p class="footer__text">© 2023 ОБУ ИТЦ. Все права защищены.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "v-Footer",
};
</script>

<style lang = "scss">
@import "../assets/styles/styles";

.footer__text {
  margin-top: 170px;
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  color: $greyColor;
}
</style>