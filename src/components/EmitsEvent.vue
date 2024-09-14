<template>
    <div class="component">
        <h1>Componente que emite evento</h1>
        <p>{{ item }} (R${{ price?.toFixed(2) }})</p>
        <button @click="handleAddCart">Add ao Carrinho</button>
    </div>
</template>

<script lang="ts" setup>
const props = defineProps(
    {
        item: String,
        price: Number
    }
)
const emit = defineEmits((["addCart", "removeCart"]))

function handleAddCart() {
    emit("addCart", props.price)
}
</script>