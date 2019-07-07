<template>
  <v-app>
    <v-toolbar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>SOA</span>
        <span class="font-weight-light"> ISW</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        flat
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
      >
        <span class="mr-2">PROFE DUARTE</span>
      </v-btn>
    </v-toolbar>

    <v-content>
      <traerUsuario/>
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import traerUsuario from './components/traerUsuario'
export default {
  name: 'App',
  components: {
    traerUsuario
  },
  data () {
    return {
      //
    }
  }
}
</script>
