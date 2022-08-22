<template>
  <nav>
    <h2 class="title">Crypto<span>Smart</span></h2>

    <div class="menu-links">
      <a href="#" class="active">Home</a>
      <a href="#">Businesses</a>
      <a href="#">Trade</a>
      <a href="#">Market</a>
      <a href="#">Learn</a>
    </div>

    <div class="right">
      <div class="lang">
        <img src="../assets/svg/world.svg" />
        <p>EN</p>
        <span></span>
      </div>

      <button-comp text="Login" />
    </div>
  </nav>
</template>

<script>
import ButtonComp from "./ButtonComp.vue";
export default {
  name: "HeaderNav",
  components: {
    ButtonComp,
  },
};
</script>

<style scoped>
@import "../css/variables.css";

nav {
  /* display: grid;
  grid-template-columns: repeat(3, 1fr); */
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 100px;
  padding: 0 2rem;
  background: transparent;
  position: fixed;
  top: 0;
  width: 100%;
}

.title {
  color: aliceblue;
  font-family: RalewayBlack;
}
.title span {
  color: var(--c-accent);
}

.menu-links {
  display: flex;
  gap: 2rem;
  align-items: center;
}

.menu-links a {
  color: aliceblue;
}
.menu-links a.active {
  color: var(--c-accent);
}

.lang {
  display: flex;
  gap: 0.5rem;
  align-items: center;
}
.lang span {
  height: 8px;
  width: 8px;
  border-left: 1px solid aliceblue;
  border-bottom: 1px solid aliceblue;
  transform: rotate(-45deg);
  margin-top: -5px;
}

.right {
  display: flex;
  gap: 10px;
}
</style>