<template>
  <div id="app">
    <geolocation />
  </div>
</template>

<script>
import Geolocation from './components/Geolocation.vue'

export default {
  name: 'App',
  head: {
    meta: [
      {charset: 'utf-8'},
      {name: 'viewport', content: 'width=device-width, initial-scale=1'}
    ],
  },
  components: {
    Geolocation
  }
}
</script>

<style lang="sass">
@import "../node_modules/bulma/bulma.sass";
</style>
