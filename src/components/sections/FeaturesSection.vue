<script>
import { defineComponent } from "vue";
import FeatureCard from "../FeatureCard.vue";
import ButtonComp from "../ButtonComp.vue";

export default defineComponent({
  setup() {
    const features = [
      {
        name: "Manage Portfolio",
        desc: "Buy and sell popular digital currencies, keep track of them in the one place.",
        icon: "./img/features/manage.svg",
      },
      {
        name: "Protected Securely",
        desc: "All cash balances are covered by FDIC insurance, up to a maximum of $250,000.",
        icon: "./img/features/security.svg",
      },
      {
        name: "Cryptocurrency Variety",
        desc: "Supports a variety of the most popular digital currencies and always uptodate.",
        icon: "./img/features/crypto.svg",
      },
      {
        name: "Learn Best Practice",
        desc: "Easy to know how to cryptocurrency works and friendly to newbie.",
        icon: "./img/features/learn.svg",
      },
    ];

    return { features };
  },
  components: {
    FeatureCard,
    ButtonComp
},
});
</script>

<template>
  <section>
    <div class="header">
      <h1>CryptoCap Amazing Faetures</h1>
      <p>
        Explore sensational features to prepare your best investment in
        cryptocurrency
      </p>
    </div>
    <div class="features">
      <feature-card
        v-for="feature in features"
        :key="feature.name"
        :name="feature.name"
        :desc="feature.desc"
        :icon="feature.icon"
      />
    </div>
    <div class="explore">
      <div class="left">
        <h3>New In Cryptocurrency?</h3>
        <p>We'll tell you what cryptocurrencies are, how they work and why you should own one right now. So let's do it.</p>
      </div>
      <ButtonComp text="Learn & Explore Now" glow />
    </div>
  </section>
</template>

<style scoped>
section {
  background: rgb(50, 1, 40);
  background: radial-gradient(
    circle,
    rgba(24, 3, 43, 1) 46%,
    rgba(19, 1, 34, 1) 100%
  );
}
.features {
  display: flex;
  justify-content: space-around;
}
.header {
  text-align: center;
  padding: 3rem 0;
}
.explore{
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 8rem 4rem;
}
.explore .left{
  max-width: 800px;
  line-height: 1.5rem;
}
@media (max-width: 1329px){
  .features{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    place-items: center;
    gap: 1rem;
  }
}
</style>