<script>
import { defineComponent } from "vue";
import FeatureCard from "../FeatureCard.vue";

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
        icon: "./img/features/manage.svg",
      },
      {
        name: "Cryptocurrency Variety",
        desc: "Supports a variety of the most popular digital currencies and always uptodate.",
        icon: "./img/features/manage.svg",
      },
    ];

    return { features };
  },
  components: {
    FeatureCard,
  },
});
</script>

<template>
  <section>
    <div class="features">
      <feature-card
        v-for="feature in features"
        :key="feature.name"
        :name="feature.name"
        :desc="feature.desc"
        :icon="feature.icon"
      />
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
</style>