<template>
  <div class="button">
    <div class="filters" @click="showList">
      <div class="filters__content">
        <img src="../assets/image/settings.svg" alt="filters">
        <p>Фильтры</p>
      </div>
    </div>

    <ul v-if="statusShow">
      <li v-for="(list, index) in lists" :key="index"> <input type="checkbox">{{ list }}</li>
    </ul>
  </div>
</template>

<script>


export default {
  name: "buttonItem",
  data() {
    return {
      lists: [
        'Акне Студия', 'АМИ Париж', 'Вквадрате2', 'Каменный остров'
      ],
      statusShow: false,
    }
  },
  methods: {
    showList() {
      this.statusShow = !this.statusShow;
    },

  },

}
</script>

<style lang="scss" scoped>
.button {
  margin-top: 32px;

  .filters {
    display: inline-block;
    cursor: pointer;

    &__content {
      display: flex;
      align-items: center;
      gap: 10px;
    }
  }

  ul {
    position: absolute;
    display: flex;
    flex-direction: column;
    align-items: center;
    top: 130px;
    left: 130px;
    background-color: #fff;
    box-shadow: 0px 4px 16px rgba(0, 0, 0, 0.08);
    border-radius: 8px;
    width: 320px;
    height: 255px;
  }

  li {
    padding: 20px;
    width: 100%;
    height: 100%;
    list-style: none;

    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    transition: all .3s;
    cursor: pointer;

    &:hover {
      background: #F2F4F7;
      border-radius: 6px;
    }
  }

  input {
    margin-right: 10px;
  }
}
</style>