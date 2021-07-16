<template>
  <div class="about">
    <h1>{{contador}}</h1>
  </div>
</template>

<script>
import {mapState} from 'vuex'

export default {
  computed: {
    ...mapState(['contador'])
  }
}



</script>