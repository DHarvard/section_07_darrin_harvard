<template>
  <v-app id="app">
    <v-app-bar dark max-height="75">
      <v-toolbar-title>
        <projHeader></projHeader>
      </v-toolbar-title>
    </v-app-bar>

    <v-content>
      <v-container>
        <v-row justify="center" align-items="center">
          <v-col sm="4">
            <projServerDetails></projServerDetails>
          </v-col>
        </v-row>

        <v-row>
          <v-col sm="6" :id="'server' + i" v-for="i in 6" :key="i">
            <projServers :serverIndex="i"></projServers>
          </v-col>
        </v-row>
      </v-container>
    </v-content>

  <v-footer padless class="grey lighten-2">
    <projFooter></projFooter>
  </v-footer>

  </v-app>
</template>

<script>
  import header from './components/Shared/Header.vue';
  import footer from './components/Shared/Footer.vue';
  import servers from './components/Server/Servers.vue';
  import serverDetails from './components/Server/ServerDetails.vue';
  

    export default {
        components: {
            projHeader: header,
            projServers: servers,
            projServerDetails: serverDetails,
            projFooter: footer
        }
    };
</script>

<style scoped>

</style>