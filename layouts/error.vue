<template>
    <div >
            <div>
                <h3>error {{ error.statusCode }}</h3>
                <p v-if="error.statusCode >= 400 && error.statusCode <= 499">
                    Pagina não encontrada
                </p>
                <p v-else-if="error.statusCode >= 500 && error.statusCode <= 599">
                    Erro do Servidor Interno
                </p> 
                <p v-else>
                    Tente novamente mais tarde
                </p>
            </div>
            <NuxtLink to="/" >Voltar</NuxtLink>
    </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
    props:{
        error:{
            type: Object,
            required: true
        }
    }
})
</script>

<style lang="scss" scoped>
</style>