<template>
  <section>
    <feature-card />
  </section>
</template>

<script>
import { defineComponent } from "vue";
import FeatureCard from "../FeatureCard.vue";

export default defineComponent({
  setup() {},
  components: {
    FeatureCard,
  },
});
</script>

<style scoped>
section {
  background: rgb(50, 1, 40);
  background: radial-gradient(
    circle,
    rgba(24, 3, 43, 1) 46%,
    rgba(19, 1, 34, 1) 100%
  );
}
</style>