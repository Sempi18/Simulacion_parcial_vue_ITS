<script setup lang="ts">
import Contador from "./components/Contador.vue";
</script>

<template>
  <div class="app-container">
    <h1>SPA - Práctica Simulación Parcial</h1>
    <p class="subtitle">Vue 3 + Composition API</p>
    <Contador />
  </div>
</template>

<style scoped>
.app-container {
  max-width: 800px;
  margin: 0 auto;
}

h1 {
  color: #646cff;
  margin-bottom: 0.5rem;
}

.subtitle {
  color: #888;
  font-size: 1.2rem;
  margin-top: 0;
}
</style>
