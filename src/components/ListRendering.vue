<template>
    <div class="component">
        <h1>Componente de rederização de lista</h1>
        <p>Nome: {{ name }}</p>
        <p v-show="pets?.length === 0">Não tem animais</p>
        <ul>
            <li v-for="pet in pets">
                Nome: {{ pet.name }} |
                Idade: {{ pet.age }}
            </li>
        </ul>
    </div>
</template>

<script setup lang="ts">
defineProps({
    name: String,
    pets: Array
})
</script>

<style scoped>
ul {
    margin: 0;
    padding: 0;
}

li {
    list-style: None;
    text-align: center;
    font-size: larger;

}
</style>