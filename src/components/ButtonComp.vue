<script setup>
import { defineProps } from "vue";

const props = defineProps({
  text: String,
  glow: Boolean
});
</script>

<template>
  <button :class="{glow: props.glow}">{{ props.text }}</button>
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
.glow{
  box-shadow: 0 0 25px var(--c-accent);

}
</style>