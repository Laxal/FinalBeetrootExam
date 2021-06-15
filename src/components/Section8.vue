<template>
  <section class="section8" id="GALERIE">
    <div class="section8__img">
      <img src="../assets/img/section8-1.jpg" alt="8-1" />
    </div>
    <div class="section8__img">
      <img src="../assets/img/section8-2.jpg" alt="8-2" />
    </div>
    <div class="section8__img">
      <img src="../assets/img/section8-3.jpg" alt="8-3" />
    </div>
    <div class="section8__img">
      <img src="../assets/img/section8-4.jpg" alt="8-4" />
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.section8 {
  display: flex;

  &__img {
    max-width: 25%;
    width: 100%;

    img {
      width: 100%;
      height: auto;
      object-fit: cover;
    }
  }
}
</style>