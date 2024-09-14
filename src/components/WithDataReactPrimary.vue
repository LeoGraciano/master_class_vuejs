<template>
  <div class="component">
    <h1>Componente com dados Reativos</h1>
    <p>Nome: {{ name }} | Idade: {{ age }}</p>
    <button @click="changeName">Mudar Nome</button>
    <button v-on:click="makeBirthday">Fazer Aniversário</button>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const name = ref('Leo');
const age = ref(39);
function makeBirthday() {
  age.value++;
}

function changeName() {
  name.value = 'Leonardo';
}
</script>

<style scoped></style>
