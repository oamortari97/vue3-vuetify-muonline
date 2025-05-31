<template>
  <v-card class="mb-4 castle-siege-card">
    <v-card-title class="d-flex align-center card-title">
      <v-icon color="orange" class="mr-2">mdi-castle</v-icon>
      Castle Siege
      <v-spacer></v-spacer>
      <div class="d-flex flex-column align-end">
        <span class="text-caption text-uppercase">DOM</span>
        <span class="text-h6 error--text">2030</span>
      </div>
    </v-card-title>
    <v-card-subtitle class="pb-0">BATALHA PELO CONTROLE</v-card-subtitle>
    <v-card-text>
      <v-row>
        <v-col cols="12">
          <v-card variant="flat" color="grey-darken-4" class="pa-2">
            <div class="d-flex align-center">
              <v-icon color="amber" class="mr-2">mdi-shield-crown</v-icon>
              <div>
                <div class="text-caption text-uppercase">TESTE</div>
                <div class="text-body-2">GUILD PHOENIX - SENHOR DO CASTELO</div>
              </div>
              <v-spacer></v-spacer>
              <div class="d-flex flex-column align-end">
                <span class="text-caption text-uppercase">7 DIAS</span>
                <span class="text-caption">NO PODER</span>
              </div>
            </div>
          </v-card>
        </v-col>
      </v-row>
      <v-row class="mt-2">
        <v-col cols="12">
          <v-btn 
            block 
            color="orange-darken-4" 
            variant="elevated"
            prepend-icon="mdi-sword"
            class="text-none"
          >
            PRÓXIMA BATALHA: DOMINGO ÀS 20H
          </v-btn>
        </v-col>
      </v-row>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  name: 'CastleSiege'
}
</script>

<style scoped>
.castle-siege-card {
  border: 1px solid rgba(212, 175, 55, 0.3);
  background-color: #2A2A2A !important;
}
</style>
