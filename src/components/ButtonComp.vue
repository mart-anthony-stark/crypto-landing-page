<script setup>
import { defineProps } from "vue";

const props = defineProps({
  text: String,
});
</script>

<template>
  <button>{{ props.text }}</button>
</template>


<style scoped>
@import "../css/variables.css";

button {
  padding: 10px 20px;
  border: none;
  background: var(--c-accent);
  border-radius: 5px;
  color: aliceblue;
  cursor: pointer;
}
</style>