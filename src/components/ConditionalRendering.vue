<template>
    <div class="component">
        <h1>Componente de rederização condicional</h1>
        <p>Nome: {{ name }}</p>
        <p v-if="qtyPets === 1">Tem Animal</p>
        <p v-else-if="qtyPets > 1">Tem muitos Animais</p>
        <p v-else="qtyPets === 0">Não tem Animais</p>
    </div>
</template>

<script setup lang="ts">
defineProps({
    name: String,
    qtyPets: Number
})
</script>