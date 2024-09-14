<template>
  <div class="component">
    <h1>Componente com dados Reativos Não Primitivos</h1>
    <p>Nome: {{ pessoa.name }} | Idade: {{ pessoa.age }}</p>
    <button @click="changeName()">Mudar Nome</button>
    <button @click="makeBirthday">Fazer Aniversário</button>
  </div>
</template>

<script setup lang="ts">
import { reactive } from 'vue';
const pessoa = reactive({ name: "Ana", age: 27 })

function makeBirthday() {
  pessoa.age++;
}

function changeName() {
  pessoa.name = 'Ana Maria';
}
</script>

<style scoped></style>
