<template>
  <section class="section5">
    <h3 class="section5__main-title">SPECIALTIES</h3>
    <div ref="slick">
      <div>
        <div class="container section5-container">
          <div class="section5__description">
            <h2 class="section5__title">CHOCOLATE PANCAKES</h2>
            <h3 class="section5__subtitle">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis at
              velit maximus, molestie est a, tempor magna.
            </h3>
            <p class="section5__text">
              Integer ullamcorper neque eu purus euismod, ac faucibus mauris
              posuere. Morbi non ultrices ligula. Sed dictum, enim sed
              ullamcorper feugiat, dui odio vehicula eros, a sollicitudin lorem
              quam nec sem. Mauris tincidunt feugiat diam convallis pharetra.
              Nulla facilisis semper laoreet.
            </p>
          </div>
          <div class="section5__img">
            <img src="../assets/img/section5.jpg" alt="our team" />
          </div>
        </div>
      </div>
      <div>
        <div class="container section5-container">
          <div class="section5__description">
            <h2 class="section5__title">CHOCOLATE PANCAKES</h2>
            <h3 class="section5__subtitle">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis at
              velit maximus, molestie est a, tempor magna.
            </h3>
            <p class="section5__text">
              Integer ullamcorper neque eu purus euismod, ac faucibus mauris
              posuere. Morbi non ultrices ligula. Sed dictum, enim sed
              ullamcorper feugiat, dui odio vehicula eros, a sollicitudin lorem
              quam nec sem. Mauris tincidunt feugiat diam convallis pharetra.
              Nulla facilisis semper laoreet.
            </p>
          </div>
          <div class="section5__img">
            <img src="../assets/img/section5.jpg" alt="our team" />
          </div>
        </div>
      </div>
      <div>
        <div class="container section5-container">
          <div class="section5__description">
            <h2 class="section5__title">CHOCOLATE PANCAKES</h2>
            <h3 class="section5__subtitle">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis at
              velit maximus, molestie est a, tempor magna.
            </h3>
            <p class="section5__text">
              Integer ullamcorper neque eu purus euismod, ac faucibus mauris
              posuere. Morbi non ultrices ligula. Sed dictum, enim sed
              ullamcorper feugiat, dui odio vehicula eros, a sollicitudin lorem
              quam nec sem. Mauris tincidunt feugiat diam convallis pharetra.
              Nulla facilisis semper laoreet.
            </p>
          </div>
          <div class="section5__img">
            <img src="../assets/img/section5.jpg" alt="our team" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  mounted() {
    window.$(this.$refs.slick).slick({
      dots: true,
      // infinite: true,
      // autoplay: true,
      autoplaySpeed: 4000,
      dotsClass: "slick-dots",
    });
  },
};
</script>

<style lang="scss" scoped>
.section5 {
  position: relative;
  background: url("../assets/img/section5-bg.jpg") center / cover no-repeat;
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
.custom-dots {
  background-color: #00f;
  widows: 200px;
  height: 100px;
}
</style>