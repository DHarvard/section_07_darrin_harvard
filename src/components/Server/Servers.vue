<template>
  <v-container>
    <v-row justify="center">
      <v-col sm="6">
        <v-card hover ripple>
          <v-card-title justify="left">Server #{{ serverIndex }}</v-card-title>
          <v-card-text justify="left">Server Status</v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  props: {
    serverIndex: Number,
  },
  data: () => ({
  })
};
</script>

<style scoped>
</style>
