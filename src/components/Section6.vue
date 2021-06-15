<template>
  <section class="section6" id="MENU">
    <div class="container">
      <h2 class="section6__title">DELICIOUS MENU</h2>
      <h3 class="section6__subtitle">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis at velit
        maximus, molestie est a, tempor magna.
      </h3>
      <div class="section6__tabs">
        <ul class="menu-categories">
          <li
            class="menu-categories__item"
            v-for="item in menuCategories"
            :key="item"
          >
            {{ item }}
          </li>
        </ul>
        <div class="menu-list">
          <ul class="menu-list__section" v-for="section in 3" :key="section">
            <li
              class="menu-list__item"
              v-for="(menuItem, i) in menuListForPizza"
              :key="i"
            >
              <h4>{{ menuItem.name }} .... {{ menuItem.price }}</h4>
              <p>{{ menuItem.deskription }}</p>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      menuCategories: [
        "SOUPE",
        "PIZZA",
        "PASTA",
        "DESERT",
        "WINE",
        "BEER",
        "DRINKS",
      ],

      menuListForPizza: [],
    };
  },

  created() {
    let pizzaItem = {
      name: "PIZZA QUATRO STAGIONI",
      price: "55,68 USD",
      deskription: "Integer ullamcorper neque eu purus euismod",
    };

    for (let i = 0; i < 7; i++) {
      this.menuListForPizza.push(pizzaItem);
    }
  },
};
</script>

<style lang="scss" scoped>
.section6 {
  position: relative;
  padding: 100px 0;

  &__title {
    position: relative;
    font-family: "Dosis", sans-serif;
    font-style: normal;
    font-weight: bold;
    font-size: 36px;
    line-height: 48px;
    padding: 12px 0;
    text-align: center;
    color: #000;
    margin-bottom: 25px;

    &::before {
      content: "";
      display: block;
      position: absolute;
      bottom: 0;
      left: 50%;
      transform: translateX(-50%);
      width: 60px;
      height: 5px;
      background: #e8c300;
      border-radius: 50px;
    }
  }
  &__subtitle {
    font-family: "Open Sans", sans-serif;
    font-style: normal;
    font-weight: bold;
    font-size: 18px;
    line-height: 28px;
    text-align: center;
    color: #000;
    margin-bottom: 30px;
    max-width: 50%;
    margin: 0 auto;
    margin-bottom: 50px;
  }

  .menu-categories {
    display: flex;
    justify-content: center;
    margin-bottom: 50px;

    &__item {
      padding: 20px 0;
      font-family: "Open Sans", sans-serif;
      font-style: normal;
      font-weight: bold;
      font-size: 12px;
      line-height: 12px;
      text-align: center;
      color: #333333;
      max-width: 120px;
      width: 100%;
      transition: all 0.3s ease;

      &:hover,
      &:active,
      &:focus {
        cursor: pointer;
        background-color: #ccc;
      }

      &:not(:last-child) {
        border-right: 1px solid rgba(51, 51, 51, 0.2);
      }
    }
  }

  .menu-list {
    display: flex;
    justify-content: space-between;

    &__item {
      margin-bottom: 35px;

      h4 {
        font-family: "Dosis", sans-serif;
        font-style: normal;
        font-weight: 500;
        font-size: 18px;
        line-height: 18px;

        color: #333333;
      }

      p {
        font-family: "Open Sans", sans-serif;
        font-style: normal;
        font-weight: 400;
        font-size: 12px;
        line-height: 18px;

        color: rgba($color: #333, $alpha: 0.5);
      }
    }
  }
}
</style>