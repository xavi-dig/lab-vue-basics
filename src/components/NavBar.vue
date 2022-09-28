<template>
  <nav v-if="isHome === true">
    <ul>
      <li>Page 1</li>
      <li>Page 2</li>
      <li>Page 3</li>
    </ul>
  </nav>
  <nav v-else>
    <ul>
      <li>Home</li>
      <li></li>
      <li></li>
    </ul>
  </nav>
  <!-- IT 4 -->
  <div v-for="(post, index) in posts" :key="index">
    <ul>
      <li>
        <h3>Title: {{ post.title }}</h3>
        <p>Description: {{ post.description }}</p>
        <p>Content: {{ post.content }}</p>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from "vue";
const isHome = ref(true);
const posts = ref([
  {
    title: "Iros todos a tomar por culo",
    description: "Disco de Extremoduro",
    content: "Disco de canciones grabadas en diferentes conciertos",
  },
  {
    title: "Mierda",
    description: "Disco de DobleV",
    content: "Uno de los mejores discos de este grupo de Hip Hop Español",
  },
  {
    title: "Lo más lejos a tu lado",
    description: "Disco de Fito & Fitipaldis",
    content: "Disco que a principio de los 2000 lanzó a la fama a este grupo",
  },
]);
</script>

<style scoped></style>
