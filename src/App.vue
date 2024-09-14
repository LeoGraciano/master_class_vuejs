<script setup lang="ts">
import WithData from './components/WithData.vue';
import WithDataReactPrimary from './components/WithDataReactPrimary.vue';
import FirstComponent from './components/FirstComponent.vue';
import WithDataReactNotPrimary from './components/WithDataReactNotPrimary.vue';
import DataBinding from './components/DataBinding.vue';
import WithProps from './components/WithProps.vue';
import ListenEvent from './components/ListenEvent.vue';
import ComputedProperties from './components/ComputedProperties.vue';
import WatchProperties from './components/WatchProperties.vue';
import ConditionalRendering from './components/ConditionalRendering.vue';
import ListRendering from './components/ListRendering.vue';
import Slots from './components/Slots.vue';
const itemProps = 'Borracha'
const priceProps = 2.50

const pets = [{ name: 'Perro', age: 1 }, { name: 'Gato', age: 5 }, { name: 'Pez', age: 13 }]
</script>

<template>
  <header>Vue</header>
  <Slots>
    <template v-slot:icon>
      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
        stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
        class="icon icon-tabler icons-tabler-outline icon-tabler-home">
        <path stroke="none" d="M0 0h24v24H0z" fill="none" />
        <path d="M5 12l-2 0l9 -9l9 9l-2 0" />
        <path d="M5 12v7a2 2 0 0 0 2 2h10a2 2 0 0 0 2 -2v-7" />
        <path d="M9 21v-6a2 2 0 0 1 2 -2h2a2 2 0 0 1 2 2v6" />
      </svg>
    </template>

  </Slots>
  <Slots>
    <template v-slot:icon>
      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
        stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
        class="icon icon-tabler icons-tabler-outline icon-tabler-home">
        <path stroke="none" d="M0 0h24v24H0z" fill="none" />
        <path d="M5 12l-2 0l9 -9l9 9l-2 0" />
        <path d="M5 12v7a2 2 0 0 0 2 2h10a2 2 0 0 0 2 -2v-7" />
        <path d="M9 21v-6a2 2 0 0 1 2 -2h2a2 2 0 0 1 2 2v6" />
      </svg>
    </template>
    <template v-slot:text>
      Home
    </template>
  </Slots>
  <ListRendering name="Paulo" :pets="pets" />
  <ConditionalRendering name="Paulo" :qtyPets="2" />
  <WatchProperties />
  <ComputedProperties />
  <ListenEvent />
  <WithProps :item="itemProps" :price="priceProps" />
  <DataBinding />
  <WithDataReactNotPrimary />
  <WithDataReactPrimary />
  <WithData />
  <FirstComponent />
</template>

<style scoped></style>
