<template>
  <header-nav />
  <hero-page />
  <features-section />
</template>

<script>
import HeaderNav from "./components/HeaderNav.vue";
import HeroPage from "./components/HeroPage.vue";
import FeaturesSection from "./components/sections/FeaturesSection.vue";

export default {
  name: "App",
  components: {
    HeaderNav,
    HeroPage,
    FeaturesSection,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@300;400&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
a {
  text-decoration: none;
}

li {
  list-style: none;
}
@font-face {
  font-family: RalewayBlack;
  src: url("./fonts/static/Raleway-Black.ttf");
}
@font-face {
  font-family: Raleway;
  src: url("./fonts/Raleway-VariableFont_wght.ttf");
}

body {
  font-family: Raleway;
  color: aliceblue;
}

section {
  min-height: 100vh;
}
</style>
