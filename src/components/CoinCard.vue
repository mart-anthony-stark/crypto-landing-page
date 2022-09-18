<script setup>
import { defineProps } from "vue";

const props = defineProps({
  name: String,
  slug: String,
  img: String,
  value: String,
  rate: String,
});
</script>

<template>
  <div class="cont">
    <div class="head">
      <img :src="props.img" class="coin-img" />

      <div class="name">
        <span class="coin">{{ props.slug.toUpperCase() }}</span>
        <span>{{ props.name.toUpperCase() }}</span>
      </div>

      <img src="../assets/coins/see-more-ic.png" alt="" />
    </div>

    <div class="bottom">
      <div class="stats">
        <h4>{{ props.value }}</h4>
        <span>{{ props.rate }}</span>
      </div>

      <img src="../assets/coins/chart-state1.png" alt="" />
    </div>
  </div>
</template>

<style scoped>
.cont {
  width: 297px;
  height: 187px;

  /* High Fidelity Color/Card Background */

  background: rgba(255, 255, 255, 0.02);
  border: 1px solid rgba(255, 255, 255, 0.05);
  border-radius: 18px;
  padding: 0.3rem 1rem;
  font-family: "Roboto", sans-serif;
}

.head {
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-bottom: 1px solid rgba(131, 131, 131, 0.473);
  padding-bottom: 0.5rem;
  margin-bottom: 0.5rem;
}
.coin-img {
  height: 30px;
  width: 30px;
}

.name {
  display: flex;
  gap: 10px;
  align-items: center;
}
.name span:nth-child(1) {
  font-weight: 900;
}
.name span:nth-child(2) {
  background: rgb(204, 204, 204);
  border-radius: 3px;
  color: black;
  font-size: 8px;
  padding: 5px;
}

.bottom {
  display: grid;
  grid-template-columns: 1fr 1fr;
}
.bottom .stats {
  line-height: 2rem;
}
.bottom .stats span {
  font-size: 14px;
  color: gray;
}
</style>