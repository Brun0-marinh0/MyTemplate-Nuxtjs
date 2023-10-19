<template>
    <div class="containerRouters">
        <div v-for="router in routers" :key="router.name">
            <NuxtLink class="pill" :to="getLink(router.link)">{{ router.name }}</NuxtLink>
        </div>
    </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
    data(){
        return{
            routers:[
                {name: 'link teste de error', link: 'error'}
            ]
        }
    },
    methods:{
        getLink(link: String){
            if(link === 'error'){
                return link
            }
        }
    }
})
</script>

<style lang="scss" scoped>
    .containerRouters{
        display: flex;
        gap: 0.5rem;
        align-items: center;
        height: 4rem;
    }
    a{
        border: 1px solid var(--bgMain);
        color: var(--bgMain);
    }
</style>