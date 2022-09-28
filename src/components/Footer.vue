<template>
  <footer v-show="showIt">
    <p :class="clickedButton && 'backgroundColor'">Esto es un footer</p>
    <!-- IT 2.1 -->
    <p>{{ 2 + 2 }}</p>
    <button @click="click()">CLICK ME!</button>
  </footer>
</template>

<script setup>
import { ref } from "vue";
const showIt = ref(true);
const clickedButton = ref(false);
function click() {
  clickedButton.value = !clickedButton.value;
}
</script>

<style scoped>
.backgroundColor {
  background-color: blue;
  color: white;
}
</style>
