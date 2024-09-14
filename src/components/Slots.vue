<template>
    <div class="component">
        <h1>Componente com Slots</h1>
        <button>
            <slot name="icon" />
            <slot name="text">Valor Parão</slot>
        </button>
    </div>
</template>