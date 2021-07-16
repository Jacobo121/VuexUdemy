<template lang="">
    <div>
        <button
            @click="accionBoton({estado: estado, numero: 5})"
        >{{textoButton}}</button>
    </div>
</template>
<script>
import {mapActions} from 'vuex'

export default {
    props: {
        estado: Boolean
    },
    computed: {
        textoButton() {
            return this.estado ? 'Aumentar' : 'Disminuir'
        }
    },

    methods: {
        ...mapActions(['accionBoton'])
    }
}
</script>
<style lang="">
    
</style>