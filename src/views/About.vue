<template>
  <div class="about">
    <h1>{{contador}}</h1>
    <input type="text" v-model="texto" />
    <h2>{{texto}}</h2>
  </div>
</template>

<script>
import {mapState} from 'vuex'

export default {

  data() {
    return {
      texto: ''
    }
  },

  computed: {
    ...mapState(['contador'])
  }
}



</script>