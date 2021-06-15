<template>
  <a href="#CONTACT" class="header__scroll"></a>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.header__scroll {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  bottom: 40px;

  display: block;
  width: 40px;
  height: 40px;
  background-color: #fff;
  border-radius: 50%;

  &::before {
    content: "";
    display: block;
    position: absolute;
    top: 45%;
    left: 50%;
    transform: translate(-50%, -50%) rotate(45deg);

    width: 10px;
    height: 10px;
    border: 4px solid #333;
    border-top: none;
    border-left: none;
  }

  &::after {
    content: "";
    display: block;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);

    width: 60px;
    height: 60px;
    border: 1px solid rgba($color: #fff, $alpha: 0.2);
    border-radius: 50%;
  }
}
</style>