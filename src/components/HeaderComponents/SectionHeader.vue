<template>
  <header id="HOME">
    <a href="#"
      ><img src="../../assets/img/Logo.svg" alt="Logo" class="logo"
    /></a>
    <div class="container">
      <header-nav />
      <div class="header__content">
        <p class="header__work-shedule">
          Mon - Fri: 8PM - 10PM, Sat - Sun: 8PM - 3AM
        </p>
        <header-main />
        <header-social />
      </div>
    </div>
    <header-scroll />
  </header>
</template>

<script>
import HeaderMain from "./HeaderMain.vue";
import HeaderNav from "./HeaderNav.vue";
import HeaderScroll from "./HeaderScroll.vue";
import HeaderSocial from "./HeaderSocial.vue";

export default {
  components: { HeaderNav, HeaderSocial, HeaderMain, HeaderScroll },
};
</script>

<style lang="scss" scoped>
header {
  padding: 100px 0;
  position: relative;
  height: 800px;
  background: #123 url("../../assets/img/header-bg.jpg") center / cover
    no-repeat;

  img {
    position: absolute;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
  }

  .header__content {
    display: flex;
    justify-content: space-between;
    transform: translateY(100%);
  }

  .header__work-shedule {
    display: inline-block;
    white-space: nowrap;
    font-family: "Open Sans", sans-serif;
    font-style: normal;
    font-weight: bold;
    font-size: 12px;
    line-height: 12px;
    color: #ffffff;
    transform: rotate(-90deg);
  }
}
</style>
