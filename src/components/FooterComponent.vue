<template>
  <footer>
    <p>© Copyright <span> Mindblister</span> 2019</p>
  </footer>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
footer {
  background-color: rgba($color: #000000, $alpha: 0.9);
  height: 100px;
  display: flex;
  justify-content: center;
  align-items: center;

  p {
    font-family: "Open Sans", sans-serif;
    font-style: normal;
    font-weight: normal;
    font-size: 12px;
    line-height: 12px;

    color: rgba(255, 255, 255, 0.5);

    border-radius: 5px;

    span {
      font-weight: 700;
    }
  }
}
</style>