<template>
  <section class="section7" id="EVENTS">
    <h3 class="section7__main-title">PRIVATE EVENTS</h3>
    <div class="container section7-container">
      <div class="section7__img">
        <div class="event-title">WEDDING</div>
        <img src="../assets/img/section7-wedding.jpg" alt="wedding" />
      </div>
      <div class="section7__img section7__img--right">
        <div class="event-title">CORPORATE PARTIES</div>
        <img src="../assets/img/section7-corporate.jpg" alt="corporate" />
      </div>
    </div>
    <p class="event-contact">
      For private events please call:
      <a href="tel:+40729131637">+40 729 131 637</a>/<a href="tel:+40726458782"
        >+40 726 458 782</a
      >
      or use the contact form.
    </p>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.section7 {
  position: relative;
  background: url("../assets/img/section7-bg.jpg") center / cover no-repeat;
  padding: 100px 125px;

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
    align-items: center;
    & > :not(:last-child) {
      margin-right: 80px;
    }
  }

  &__img {
    position: relative;
    flex: 1;

    .event-title {
      background-color: #000;
      display: flex;
      align-items: center;
      padding: 0 20px;

      position: absolute;
      top: 52.2%;
      right: -50%;
      z-index: 5;
      transform: rotate(90deg) translate(-9%, 50%);
      height: 80px;
      width: 100%;

      font-family: "Dosis", sans-serif;
      font-style: normal;
      font-weight: 500;
      font-size: 24px;
      line-height: 12px;
      text-indent: 20px;
      color: #ffffff;
    }

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
      transform: translate(-50%, -50%);
    }

    img {
      width: 100%;
      height: auto;
      filter: drop-shadow(0px 0px 50px rgba(0, 0, 0, 0.5));
      border-radius: 5px;
    }

    &--right {
      &::before {
        left: auto;
        right: 0;
        transform: translate(50%, -50%);
      }

      .event-title {
        left: -51%;
        z-index: 5;
        transform: rotate(-90deg) translate(9%, 50%);
      }
    }
  }

  .event-contact {
    position: absolute;
    bottom: 40px;
    left: 50%;
    transform: translateX(-50%);

    font-family: "Open Sans", sans-serif;
    font-style: normal;
    font-weight: normal;
    font-size: 12px;
    line-height: 1;
    color: rgba($color: #fff, $alpha: 0.5);

    a {
      font-weight: 700;
      color: rgba($color: #fff, $alpha: 0.5);
      text-decoration: none;
    }
  }
}
</style>