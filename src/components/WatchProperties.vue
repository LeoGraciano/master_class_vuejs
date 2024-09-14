<template>
    <div class="component">
        <h1>Componente com Propriedades Assistidas</h1>
        <p>{{ age }}</p>
        <label for="">Ano Nascimento:</label>
        <input type="number" v-model="yearBirthday" min="1900">
        <label for="">Ano Atual:</label>
        <input type="number" v-model="yearCurrent" min="2000">
    </div>
</template>

<script setup>
import { ref } from 'vue';
import { watchEffect } from 'vue';
// import { watch } from 'vue';


const yearBirthday = ref(1900);
const yearCurrent = ref(new Date().getFullYear());
const age = ref(0)


watchEffect(() => {
    age.value = yearCurrent.value - yearBirthday.value;
})

// watch(yearCurrent, (year) => {
//     age.value = year - yearBirthday.value;
// })
// watch(yearBirthday, (birthday) => {
//     age.value = yearCurrent.value - birthday
// })


</script>

<style scoped>
label {
    display: block;
    margin: 10px;
}
</style>