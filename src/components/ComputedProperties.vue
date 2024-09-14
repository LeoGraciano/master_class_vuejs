<template>
    <div class="component">
        <h1>Componente com Propriedades Computadas</h1>
        <p>{{ age }}</p>
        <label for="">Ano Nascimento:</label>
        <input type="number" v-model="yearBirthday" min="1900">
        <label for="">Ano Atual:</label>
        <input type="number" v-model="yearCurrent" min="2000">
    </div>
</template>

<script setup>
import { ref, computed } from 'vue';

const yearBirthday = ref(1900);
const yearCurrent = ref(new Date().getFullYear());
const age = computed(() => { return yearCurrent.value - yearBirthday.value });

</script>

<style scoped>
label {
    display: block;
    margin: 10px;
}
</style>