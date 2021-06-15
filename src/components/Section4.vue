<template>
  <section class="section4" id="BOOKING">
    <div class="container section4-container">
      <div class="section4__description">
        <h2 class="section4__title">BOOK TABLE</h2>
        <form action="/" method="post" class="section4__form-booking">
          <input
            type="text"
            name="name"
            id="user-name"
            placeholder="Name"
            required
          />
          <input
            type="email"
            name="email"
            id="user-email"
            placeholder="Email"
            required
          />
          <input
            type="tel"
            name="tel"
            id="user-tel"
            placeholder="Phone"
            required
          />
          <select
            class="first-option"
            name="count-people"
            id="count-people"
            required
          >
            <option value="" disabled selected hidden>People</option>
            <option v-for="item in 20" :key="item" :value="item">
              {{ item + " people" }}
            </option>
          </select>
          <input
            type="text"
            name="date"
            id="booking-date"
            placeholder="Date (mm/dd)"
            required
          />
          <select class="first-option" name="time" id="booking-time">
            <option value="" selected disabled hidden>Time</option>
            <option
              v-for="(time, index) in bookingTimeArr"
              :key="index + 'time'"
              :value="time"
            >
              {{ time }}
            </option>
          </select>
          <button class="section4__button" type="submit">BOOK NOW</button>
        </form>
      </div>
      <div class="section4__img">
        <img src="../assets/img/section4.jpg" alt="about-img" />
      </div>
    </div>
    <p class="section4__contactInfo">
      Mon - Fri: <span>8PM - 10PM</span>, Sat - Sun: <span>8PM - 3AM</span>,
      Phone: <a href="tel:+40729131637">+40 729 131 637</a>/<a
        href="tel:+40726458782"
        >+40 726 458 782</a
      >
    </p>
  </section>
</template>

<script>
let bookingTimeArr = [],
  i,
  h,
  j;
for (i = 8; i < 15; i++) {
  if (i < 12) {
    h = i;
  } else if (i === 12) {
    h = "00";
  } else {
    h = "0" + (i - 12);
  }
  for (j = 0; j < 4; j++) {
    if (i === 14 && j === 3) {
      break;
    }
    bookingTimeArr.push(h + ":" + (j === 0 ? "00" : 15 * j));
  }
}

export default {
  data() {
    return {
      bookingTimeArr: bookingTimeArr,
    };
  },
};
</script>

<style lang="scss" scoped>
.section4 {
  position: relative;
  padding: 100px 0;

  &-container {
    display: flex;
    align-items: center;
    & > :not(:last-child) {
      margin-right: 80px;
    }
  }

  &__description {
    flex: 1 1 50%;
    max-width: 50%;
  }

  &__form-booking {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    width: 100%;

    & > * {
      flex: 1 1 48%;
      max-width: 48%;
      width: 100%;
      margin: 5px;
      padding: 20px;
      border: none;
      outline: none;

      font-family: "Open Sans", sans-serif;
      font-style: normal;
      font-weight: normal;
      font-size: 14px;
      line-height: 20px;
      text-indent: 20px;
      color: rgb(51, 51, 51);

      &::placeholder {
        color: rgba(51, 51, 51, 0.5);
      }

      &:hover,
      &:focus,
      &:active {
        background-color: #d1d1d1;
      }

      &.first-option {
        font-family: "Open Sans", sans-serif;
        font-style: normal;
        font-weight: normal;
        font-size: 14px;
        line-height: 20px;
        text-indent: 20px;
        color: rgba(51, 51, 51, 0.5);
      }

      background: #e5e5e5;
      border-radius: 5px;
    }

    .section4__button {
      flex: 1 1 100%;
      max-width: 100%;
      width: 100%;

      display: flex;
      justify-content: center;
      align-items: center;
      height: 60px;
      border-radius: 5px;
      font-family: "Open Sans", sans-serif;
      font-style: normal;
      font-weight: bold;
      font-size: 12px;
      line-height: 20px;
      color: #fff;
      text-decoration: none;
      background-color: #e8c300;
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
    color: #000000;
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

  &__img {
    position: relative;
    flex: 1;
    padding: 0 125px 0 0;

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
      right: 0;
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

  &__contactInfo {
    position: absolute;
    bottom: 40px;
    left: 50%;
    transform: translateX(-50%);

    font-family: "Open Sans", sans-serif;
    font-style: normal;
    font-weight: normal;
    font-size: 12px;
    line-height: 1;
    color: rgba(51, 51, 51, 0.5);

    span,
    a {
      font-weight: 700;
      color: rgba(51, 51, 51, 0.5);
      text-decoration: none;
    }
  }
}
</style>