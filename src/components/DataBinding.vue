<template>
    <div class="component">
        <h1>Componente com Data Binding</h1>
        <p>{{ value }}</p>
        <!-- <input type="text" v-bind:value="value"> -->
        <!-- <input type="text" v-bind:value="value" v-on:input="(e) => value = e.target.value"> -->
        <!-- <input type="text" :value="value" @input="(e) => value = e.target.value"> -->
        <input type="text" v-model="value">
    </div>
</template>

<script>
export default {
    data() {
        return {
            value: "Vue é muito legal!"
        }
    }
}
</script>

<style lang="stylus" scoped>

</style>