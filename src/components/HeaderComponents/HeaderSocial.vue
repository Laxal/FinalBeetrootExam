<template>
  <div class="header__social">
    <a
      href="https://www.facebook.com/"
      target="_blank"
      rel="noopener noreferrer"
      ><i class="fab fa-facebook-f"></i
    ></a>
    <a href="https://twitter.com/" target="_blank" rel="noopener noreferrer"
      ><i class="fab fa-twitter"></i
    ></a>
    <a
      href="https://www.instagram.com/"
      target="_blank"
      rel="noopener noreferrer"
      ><i class="fab fa-instagram"></i
    ></a>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.header__social {
  position: relative;
  z-index: 1;
  a {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 60px;
    height: 60px;
    border: 1px solid rgba($color: #fff, $alpha: 0.5);
    border-radius: 50%;
    background-color: transparent;

    color: #fff;
    font-size: 20px;
    line-height: 23px;
    text-decoration: none;

    &:not(:last-child) {
      margin-bottom: 20px;
    }

    i {
      transition: all 0.3s ease;
    }

    &:active,
    &:focus,
    &:hover {
      .fa-twitter {
        color: #1da1f2;
      }
      .fa-facebook-f {
        color: #4267b2;
      }
      .fa-instagram {
        color: #c13584;
      }
    }
  }
}
</style>