<template lang="">
    <div>
        <button @click="disminuirContador(50)">Disminuir</button>
    </div>
</template>
<script>
import {mapActions} from 'vuex'

export default {
    
    methods: {
        ...mapActions(['disminuirContador'])
    }
}
</script>
<style lang="">
    
</style>