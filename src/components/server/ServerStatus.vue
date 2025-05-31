<template>
  <v-card class="mb-4 server-status-card">
    <v-card-title class="d-flex align-center card-title">
      <v-icon color="success" class="mr-2">mdi-circle</v-icon>
      Servidor Principal
      <v-chip color="success" size="small" class="ml-2">ONLINE</v-chip>
    </v-card-title>
    <v-card-text>
      <v-row>
        <v-col cols="6">
          <div class="d-flex flex-column align-center">
            <v-icon color="primary" size="x-large">mdi-account-group</v-icon>
            <div class="text-h4 primary--text font-weight-bold">150</div>
            <div class="text-caption text-uppercase">JOGADORES ONLINE</div>
          </div>
        </v-col>
        <v-col cols="6">
          <div class="d-flex flex-column align-center">
            <v-icon color="primary" size="x-large">mdi-clock-outline</v-icon>
            <div class="text-h4 primary--text font-weight-bold">98%</div>
            <div class="text-caption text-uppercase">UPTIME</div>
          </div>
        </v-col>
      </v-row>
      <v-row class="mt-2">
        <v-col cols="12">
          <v-progress-linear model-value="30" height="10" color="primary" bg-color="grey-darken-3"
            rounded></v-progress-linear>
          <div class="d-flex justify-space-between mt-1">
            <span class="text-caption">0</span>
            <span class="text-caption">CAPACIDADE: 500</span>
          </div>
        </v-col>
      </v-row>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  name: 'ServerStatus'
}
</script>

<style scoped>
.server-status-card {
  border: 1px solid rgba(212, 175, 55, 0.3);
  background-color: #2A2A2A !important;
}
</style>
