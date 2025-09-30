<script setup lang="ts">
import { ref } from "vue";
import ListaItems from "./ListaItems.vue";

const contador = ref(0);

const incrementar = () => {
  contador.value++;
};
</script>

<template>
  <div class="contador-container">
    <h2>Contador</h2>
    <div :class="contador >= 10 ? 'contador-alto' : 'contador-normal'">
      Valor: {{ contador }}
    </div>
    <button @click="incrementar">Incrementar</button>

    <ListaItems :contador="contador" />
  </div>
</template>

<style scoped>
.contador-container {
  margin: 2rem 0;
  padding: 2rem;
  border: 2px solid #646cff;
  border-radius: 8px;
}

.contador-normal {
  font-size: 2rem;
  font-weight: bold;
  color: #42b883;
  margin: 1rem 0;
  padding: 1rem;
  border-radius: 8px;
  background-color: rgba(66, 184, 131, 0.1);
}

.contador-alto {
  font-size: 2rem;
  font-weight: bold;
  color: #ff6b6b;
  margin: 1rem 0;
  padding: 1rem;
  border-radius: 8px;
  background-color: rgba(255, 107, 107, 0.1);
  animation: pulse 1s infinite;
}

@keyframes pulse {
  0%,
  100% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.05);
  }
}

button {
  margin-top: 1rem;
}
</style>
