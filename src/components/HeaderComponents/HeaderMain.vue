<template>
  <div class="header-title-group">
    <h2>RESTAURANT</h2>
    <h1>HUNGRY PEOPLE</h1>
    <header-button />
  </div>
</template>

<script>
import HeaderButton from "./HeaderButton.vue";

export default {
  components: { HeaderButton },
};
</script>

<style lang="scss" scoped>
.header-title-group {
  padding: 0;
  position: absolute;
  top: 65%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 0;
}

h2 {
  font-family: "Open Sans", sans-serif;
  font-style: normal;
  font-weight: bold;
  font-size: 12px;
  line-height: 14px;
  letter-spacing: 0.5em;
  color: #fff;
  text-align: center;
  margin-bottom: 35px;
}

h1 {
  position: relative;
  font-family: "Dosis" sans-serif;
  font-style: normal;
  font-weight: bold;
  font-size: 96px;
  line-height: 1;
  color: #fff;
  text-align: center;
  padding-bottom: 30px;
  margin-bottom: 30px;
  white-space: nowrap;

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
</style>