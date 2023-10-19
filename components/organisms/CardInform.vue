<template>
    <FrameCard>
        <div class="card">
            <MainHeader/>
            <p>Template para desenvolvimento frontend com framework Nuxtjs vue, metodologia Atomic Desing, TS, SCSS, Docker e PWA</p>
        </div>
    </FrameCard>
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
    .card{
        width: 30rem;
        border-radius: 1rem;
        background: #303030;
        padding: 1rem;

        p{
            color: var(--bgMain);
        }

        @include screen("mobile"){
            background: var(--green);
        }
    }
</style>