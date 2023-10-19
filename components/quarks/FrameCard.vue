<template>
    <section>
        <slot></slot>
    </section>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
    data(){
        return{

        }
    }
})
</script>

<style lang="scss" scoped>
    section{
        width: 100%;
        height: 100vh;
        display: grid;
        place-items: center;
    }
</style>