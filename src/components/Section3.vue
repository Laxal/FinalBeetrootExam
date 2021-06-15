<template>
  <section class="section3" id="TEAM">
    <h3 class="section3__main-title">OUR TEAM</h3>
    <div class="container section3-container">
      <div class="section3__description">
        <h2 class="section3__title">MASTER CHEF</h2>
        <h3 class="section3__subtitle">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis at velit
          maximus, molestie est a, tempor magna.
        </h3>
        <p class="section3__text">
          Integer ullamcorper neque eu purus euismod, ac faucibus mauris
          posuere. Morbi non ultrices ligula. Sed dictum, enim sed ullamcorper
          feugiat, dui odio vehicula eros, a sollicitudin lorem quam nec sem.
          Mauris tincidunt feugiat diam convallis pharetra. Nulla facilisis
          semper laoreet.
        </p>
      </div>
      <div class="section3__img">
        <img src="../assets/img/section3.jpg" alt="our team" />
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.section3 {
  position: relative;
  background: url("../assets/img/section3-bg.jpg");
  padding: 100px 0;

  &__main-title {
    position: absolute;
    top: 40px;
    left: 50%;
    transform: translateX(-50%);
    font-family: "Open Sans", sans-serif;
    font-style: normal;
    font-weight: bold;
    font-size: 12px;
    line-height: 14px;
    letter-spacing: 0.5em;
    color: #ffffff;
  }

  &-container {
    display: flex;
    flex-direction: row-reverse;
    align-items: center;
    & > :not(:first-child) {
      margin-right: 80px;
    }
  }

  &__description {
    flex: 1 1 50%;
    max-width: 50%;
  }

  &__title {
    position: relative;
    font-family: "Dosis", sans-serif;
    font-style: normal;
    font-weight: bold;
    font-size: 36px;
    line-height: 48px;
    padding: 12px 0;
    text-align: center;
    color: #fff;
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
    color: #fff;
    margin-bottom: 30px;
  }

  &__text {
    font-family: "Open Sans", sans-serif;
    font-style: normal;
    font-weight: 400;
    font-size: 18px;
    line-height: 28px;
    text-align: center;
    color: #fff;
    margin-bottom: 30px;
  }

  &__img {
    position: relative;
    flex: 1;
    padding: 0 0 0 125px;

    &::before {
      content: "";
      display: block;
      width: 250px;
      height: 250px;
      border: 20px solid #e8c300;
      filter: drop-shadow(0px 0px 100px rgba(0, 0, 0, 0.5));
      border-radius: 5px;

      position: absolute;
      z-index: 1;
      top: 50%;
      left: 0;
      transform: translateY(-50%);
    }

    img {
      position: relative;
      width: 100%;
      height: auto;
      filter: drop-shadow(0px 0px 50px rgba(0, 0, 0, 0.5));
      border-radius: 5px;
    }
  }
}
</style>