<template>
  <section class="section9" id="CONTACT">
    <div class="container section9-container">
      <div class="section9__description">
        <h2 class="section9__title">CONTACT</h2>
        <h3 class="section9__subtitle">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis at velit
          maximus, molestie est a, tempor magna.
        </h3>
      </div>
      <form action="/" method="post">
        <div class="section9__flex-input">
          <input type="text" name="user-name" placeholder="Name" required />
          <input type="email" name="user-email" placeholder="Email" required />
          <input type="tel" name="user-phone" placeholder="Phone" required />
          <textarea
            name="message"
            cols="30"
            rows="5"
            placeholder="Message"
            required
          ></textarea>
        </div>
        <div class="section9__form__footer">
          <div class="section9__contact">
            <a href="#"
              ><i class="fas fa-map-marker-alt"></i> 5th London Boulevard,
              U.K</a
            >
            <div class="tel-group">
              <i class="fas fa-phone"></i>
              <a href="tel:+40729131637">+40 729 131 637</a>/
              <a href="tel:+40726458782">+40 726 458 782</a>
            </div>
            <a href="mailto:office@mindblister.com"
              ><i class="fas fa-envelope"></i> office@mindblister.com</a
            >
          </div>
          <div class="button">
            <button type="submit">SEND MESSAGE</button>
          </div>
        </div>
      </form>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.section9 {
  padding: 100px 0;

  &__description {
    max-width: 50%;
    margin: 0 auto;
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
  &__subtitle {
    font-family: "Open Sans", sans-serif;
    font-style: normal;
    font-weight: bold;
    font-size: 18px;
    line-height: 28px;
    text-align: center;
    color: #000000;
    margin-bottom: 30px;
  }

  &__flex-input {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;

    input {
      flex: 1 1 33.3%;
      max-width: 32%;
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
      background: #e5e5e5;
      border-radius: 5px;

      &::placeholder {
        color: rgba(51, 51, 51, 0.5);
      }

      &:hover,
      &:focus,
      &:active {
        background-color: #d1d1d1;
      }
    }

    textarea {
      flex: 1 1 100%;
      max-width: 100%;
      margin: 5px;
      resize: none;

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
      background: #e5e5e5;
      border-radius: 5px;

      &::placeholder {
        color: rgba(51, 51, 51, 0.5);
      }

      &:hover,
      &:focus,
      &:active {
        background-color: #d1d1d1;
      }
    }
  }

  &__form__footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  &__contact {
    display: flex;
    max-width: 50%;
    width: 100%;
    padding-right: 10px;

    & > * {
      margin: 8px;
    }

    a {
      font-family: "Open Sans", sans-serif;
      font-weight: 700;
      font-size: 12px;
      line-height: 12px;
      text-decoration: none;
      color: rgba(51, 51, 51, 0.5);
    }
    i {
      font-style: normal;
      font-weight: 900;
      font-size: 14px;
      line-height: 14px;
      color: #e8c300;
      padding-right: 10px;
    }
  }

  .button {
    flex: 1 1 50%;
    button {
      max-width: 100%;
      width: 100%;
      margin: 5px;

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
}
</style>