<script>
import ButtonComp from "./ButtonComp.vue";
import CoinCard from "./CoinCard.vue";

export default {
  name: "HeroPage",
  components: { ButtonComp, CoinCard },
  data() {
    return {
      trends: [
        {
          name: "bitcoin",
          slug: "btc",
          img: "/img/coins/bitcoin-ic.png",
          value: "$56,623.54",
          rate: "1.41%",
        },
        {
          name: "ethereum",
          slug: "eth",
          img: "/img/coins/eth-icon.png",
          value: "$4,267.90",
          rate: "2.22%",
        },
        {
          name: "binance",
          slug: "bnb",
          img: "/img/coins/bnb-icon.png",
          value: "$587.74",
          rate: "0.82%",
        },
        {
          name: "tether",
          slug: "usdt",
          img: "/img/coins/usdt-ic.png",
          value: "$0.9998",
          rate: "0.03%",
        },
      ],
    };
  },
};
</script>

<template>
  <main>
    <div class="banner">
      <h1>Start and Build Your Crypto Portfolio Here</h1>
      <p>
        Only at CryptoSmart, you can build a good portfolio and learn best
        practices about cryptocurrency.
      </p>
      <button-comp text="Get Started" />
    </div>

    <div class="market">
      <h3>Market Trend</h3>
      <div class="coins-container">
        <coin-card
          v-for="coin in trends"
          :key="coin.name"
          :name="coin.name"
          :slug="coin.slug"
          :value="coin.value"
          :rate="coin.rate"
          :img="coin.img"
        />
      </div>
    </div>
  </main>
</template>

<style scoped>
@import "../css/variables.css";

main {
  min-height: 100vh;
  background: rgb(50, 1, 40);
  background: radial-gradient(
    circle,
    rgba(50, 1, 40, 1) 0%,
    rgba(24, 3, 43, 1) 46%,
    rgba(19, 1, 34, 1) 100%
  );
}

.banner {
  max-width: 700px;
  height: 50vh;
  padding-top: 100px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin: auto;
  gap: 1.5rem;
  text-align: center;
  align-items: center;
}

.banner h1 {
  font-family: RalewayBlack;
}

.banner p {
  color: #b6b6b6;
}

.market {
  padding: 1rem 3rem;
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.coins-container {
  display: flex;
  justify-content: center;
  gap: 3rem;
  flex-wrap: wrap;
}
</style>