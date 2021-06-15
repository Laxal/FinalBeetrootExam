<template>
  <section-header />
  <section-2 />
  <section-3 />
  <section-4 />
  <section-5 />
</template>

<script>
import SectionHeader from "@/components/HeaderComponents/SectionHeader.vue";
import Section2 from "./components/Section2.vue";
import Section3 from "./components/Section3.vue";
import Section4 from "./components/Section4.vue";
import Section5 from "./components/Section5.vue";

export default {
  name: "App",
  components: {
    SectionHeader,
    Section2,
    Section3,
    Section4,
    Section5,
  },
};
</script>

// Styles =======================================================

<style lang='scss'>
@import url("https://fonts.googleapis.com/css2?family=Dosis:wght@400;700&family=Open+Sans:wght@400;700&display=swap");
@import "@/assets/scss/style.scss";

$accentColor: #e8c300;
$hoverColor: #d88406;

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

.container {
  position: relative;
  max-width: 1300px;
  width: 100%;
  margin: 0 auto;
  padding: 0 10px;
  box-sizing: border-box;
}
</style>
