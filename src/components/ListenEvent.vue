<template>
    <div class="component">
        <h1>Componente que esculta evento</h1>
        <p>Total: R${{ total }}</p>
        <div class="list">
            <EmitsEvent item="Item 1" :price="1.99" @addCart="updateTotal" />
            <EmitsEvent item="Item 2" :price="5" @addCart="updateTotal" />
            <EmitsEvent item="Item 2" :price="10.25" @addCart="updateTotal" />
        </div>
    </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue';
import EmitsEvent from './EmitsEvent.vue';

const total = ref(0);
function updateTotal(param: number) {
    const value = total.value + param;
    total.value = +value.toFixed(2);
}

</script>

<style scoped>
.list {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}
</style>