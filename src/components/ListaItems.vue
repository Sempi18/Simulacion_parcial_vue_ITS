<script setup lang="ts">
import { ref } from "vue";

defineProps<{ contador: number }>();

const items = ref([
  "Aprender Vue con Matias",
  "Aprender a usar Composition API",
  "Practicar Reactividad en apps",
  "Usar v-for correctamente",
  "Aplicar bien clases dinámicas",
]);
</script>

<template>
  <div class="lista-container">
    <h3>Lista de Tareas</h3>
    <ul>
      <li v-for="(item, index) in items" :key="index">
        {{ item }}
      </li>
    </ul>
  </div>
</template>

<style scoped>
.lista-container {
  margin-top: 2rem;
  padding: 1.5rem;
  border: 1px solid #888;
  border-radius: 8px;
  background-color: rgba(0, 0, 0, 0.1);
}

h3 {
  margin-top: 0;
  color: #646cff;
}

ul {
  list-style-type: none;
  padding: 0;
  text-align: left;
  max-width: 300px;
  margin: 0 auto;
}

li {
  padding: 0.5rem 1rem;
  margin: 0.5rem 0;
  background-color: rgba(100, 108, 255, 0.1);
  border-radius: 4px;
  border-left: 3px solid #646cff;
  transition: transform 0.2s;
}

li:hover {
  transform: translateX(5px);
  background-color: rgba(100, 108, 255, 0.2);
}
</style>
