<template>
    <div class="component">
        <h1>Componente com Props</h1>
        <p>{{ item }} (R${{ price?.toFixed(2) }})</p>
    </div>
</template>

<script lang="ts" setup>
defineProps(
    {
        item: String,
        price: Number
    }
)
</script>