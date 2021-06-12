<template>
  <section-header />
</template>

<script>
import SectionHeader from "@/components/HeaderComponents/SectionHeader.vue";

export default {
  name: "App",
  components: {
    SectionHeader,
  },
};
</script>

// Styles =======================================================

<style lang='scss'>
@import url("https://fonts.googleapis.com/css2?family=Dosis:wght@400;700&family=Open+Sans:wght@400;700&display=swap");
@import "@/assets/scss/style.scss";

*,
*::after,
*::before {
  box-sizing: border-box;
}

a {
  outline: none;
}

html {
  scroll-behavior: smooth;
}

body {
  background-image: url("/src/assets/img/header-bg.jpg");
  height: 5000px;
}

.container {
  position: relative;
  max-width: 1300px;
  width: 100%;
  margin: 0 auto;
  padding: 0 10px;
  box-sizing: border-box;
}
</style>
