<template>
  <div class="header-title-group">
    <h2>RESTAURANT</h2>
    <h1>HUNGRY PEOPLE</h1>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.header-title-group {
  padding: 0 100px;
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
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