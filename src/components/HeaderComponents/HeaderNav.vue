<template>
  <nav class="header__nav">
    <ul class="header__nav_left">
      <li v-for="itemL in navItemsLeft" :key="itemL">
        <a :href="'#' + itemL">{{ itemL }}</a>
      </li>
    </ul>
    <ul class="header__nav_right">
      <li v-for="itemR in navItemsRight" :key="itemR">
        <a :href="'#' + itemR">{{ itemR }}</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      navItemsLeft: ["HOME", "ABOUT", "TEAM", "BOOKING"],
      navItemsRight: ["MENU", "GALERIE", "EVENTS", "CONTACT"],
    };
  },
};
</script>

<style lang="scss" scoped>
.header__nav {
  position: fixed;
  z-index: 10;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  max-width: 1300px;
  width: 100%;

  display: flex;
  justify-content: space-between;
  padding: 25px 10px;

  ul {
    flex: 1 1 40%;

    display: flex;
    justify-content: space-between;

    a {
      font-family: "Open Sans", sans-serif;
      font-style: normal;
      font-weight: 700;
      font-size: 12px;
      line-height: 18px;
      color: #fff;
      text-decoration: none;
    }
  }

  &_left {
    padding: 0 110px 0 0;
  }

  &_right {
    padding: 0 0 0 110px;
  }
}
</style>