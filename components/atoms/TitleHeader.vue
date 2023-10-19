<template>
    <div class="titleHeader" @click="home">
        <div class="containerImg">
            <img src="@/static/icon.png" alt="">
        </div>
        <h3>MyTemplate</h3>
    </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
    methods:{
        home(){
            this.$router.push({ path: '/' })
        }
    }
})
</script>

<style lang="scss" scoped>
    .titleHeader{
        background:var(--bgMain);
        padding: 1rem;
        border-radius: 1rem;
        height: 8rem;
        
        .containerImg{
            min-width: 1rem;
            width: 4rem;
            display: flex;
            align-items: center;
            img{
                width: 100%;
            }
        }
        h2{
            font-family: var(--fontLora);
            &:after{
                content: '.';
                color: var(--primary);
            }
        }
    }
</style>