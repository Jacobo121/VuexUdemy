<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <h1
      :style="colorContador"
    >{{titulo}}: {{ contador }} </h1>

    <button @click="accionIncrementar" >Incrementa el contador</button>
    <btn-disminuir></btn-disminuir>

    <hr>

    <BotonAccion :estado="true" />
    <BotonAccion :estado="false" />
  </div>
</template>

<script>
import BotonAccion from '../components/BotonAccion.vue'
import BtnDisminuir from '../components/BtnDisminuir'
import {mapState, mapMutations, mapActions} from 'vuex'

export default {
  name: 'Home',
  components: {
    BtnDisminuir,
    BotonAccion
  },

  data() {
    return {
      titulo: 'Mi contador Vuex'
    }
  },

  //para mapear el state se hace en las propiedades computadas
  computed: {
    ...mapState(['contador']),

    colorContador() {
      return [this.contador > 100 ? {'color': 'green'} : {'color': 'red'} ]
    }
  },

  //para mapear las mutaciones se hace en los metodos
  methods: {
    ...mapMutations(['incrementar']),
    ...mapActions(['accionIncrementar'])
  }
}
</script>
