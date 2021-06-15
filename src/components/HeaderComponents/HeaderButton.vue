<template>
  <div class="header__buttons-group">
    <a class="header__button_primery" href="#BOOKING">BOOK TABLE</a>
    <a class="header__button_opacity" href="#ABOUT">EXPLORE</a>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
div {
  display: flex;
  justify-content: center;

  a {
    display: flex;
    justify-content: center;
    align-items: center;
    max-width: 200px;
    width: 100%;
    height: 60px;
    border-radius: 5px;
    font-family: "Open Sans", sans-serif;
    font-style: normal;
    font-weight: bold;
    font-size: 12px;
    line-height: 20px;
    color: #fff;
    text-decoration: none;
    transition: all 0.3s ease;

    &:hover,
    &:focus,
    &:active {
      background-color: #d88406;
    }
    &:not(:last-child) {
      margin-right: 40px;
    }
  }

  .header__button_primery {
    background-color: #e8c300;
  }
  .header__button_opacity {
    background-color: transparent;
    border: 1px solid rgba($color: #fff, $alpha: 0.5);
  }
}
</style>