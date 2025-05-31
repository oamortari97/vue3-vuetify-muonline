<template>
  <v-card class="mb-4 news-list-card">
    <v-card-title class="d-flex align-center">
      <v-icon color="error" class="mr-2">mdi-newspaper-variant</v-icon>
      ÚLTIMAS NOTÍCIAS
    </v-card-title>
    <v-card-text class="pa-0">
      <v-list density="compact" bg-color="transparent">
        <!-- Notícia 1 -->
        <v-list-item>
          <v-card variant="flat" color="grey-darken-4" class="w-100 pa-2 mb-2">
            <div class="d-flex align-items-start">
              <div class="flex-grow-1">
                <div class="d-flex align-center">
                  <v-icon size="small" color="grey">mdi-calendar</v-icon>
                  <span class="text-caption ml-1">14/05/2024 às 14:30</span>
                  <v-icon size="small" color="grey" class="ml-2">mdi-account</v-icon>
                  <span class="text-caption ml-1">ADMIN</span>
                </div>
                <div class="text-subtitle-2 mt-1">GRANDE ATUALIZAÇÃO: REINO DOS DRAGÕES</div>
              </div>
              <v-btn 
                color="amber-darken-2" 
                size="small" 
                variant="tonal"
                class="ml-2 text-none"
              >
                ATUALIZAÇÃO
              </v-btn>
            </div>
          </v-card>
        </v-list-item>
        
        <!-- Notícia 2 -->
        <v-list-item>
          <v-card variant="flat" color="grey-darken-4" class="w-100 pa-2 mb-2">
            <div class="d-flex align-items-start">
              <div class="flex-grow-1">
                <div class="d-flex align-center">
                  <v-icon size="small" color="grey">mdi-calendar</v-icon>
                  <span class="text-caption ml-1">11/05/2024 às 10:15</span>
                  <v-icon size="small" color="grey" class="ml-2">mdi-account</v-icon>
                  <span class="text-caption ml-1">GM MASTER</span>
                </div>
                <div class="text-subtitle-2 mt-1">EVENTO: TORNEIO DOS CAMPEÕES</div>
              </div>
              <v-btn 
                color="error" 
                size="small" 
                variant="tonal"
                class="ml-2 text-none"
              >
                EVENTO
              </v-btn>
            </div>
          </v-card>
        </v-list-item>
        
        <!-- Notícia 3 -->
        <v-list-item>
          <v-card variant="flat" color="grey-darken-4" class="w-100 pa-2 mb-2">
            <div class="d-flex align-items-start">
              <div class="flex-grow-1">
                <div class="d-flex align-center">
                  <v-icon size="small" color="grey">mdi-calendar</v-icon>
                  <span class="text-caption ml-1">09/05/2024 às 16:45</span>
                  <v-icon size="small" color="grey" class="ml-2">mdi-account</v-icon>
                  <span class="text-caption ml-1">DEV TEAM</span>
                </div>
                <div class="text-subtitle-2 mt-1">NOVA CLASSE: NECROMANTE DAS SOMBRAS</div>
              </div>
              <v-btn 
                color="info" 
                size="small" 
                variant="tonal"
                class="ml-2 text-none"
              >
                NOVIDADE
              </v-btn>
            </div>
          </v-card>
        </v-list-item>
        
        <!-- Notícia 4 -->
        <v-list-item>
          <v-card variant="flat" color="grey-darken-4" class="w-100 pa-2 mb-2">
            <div class="d-flex align-items-start">
              <div class="flex-grow-1">
                <div class="d-flex align-center">
                  <v-icon size="small" color="grey">mdi-calendar</v-icon>
                  <span class="text-caption ml-1">01/05/2024 às 08:00</span>
                  <v-icon size="small" color="grey" class="ml-2">mdi-account</v-icon>
                  <span class="text-caption ml-1">ADMIN</span>
                </div>
                <div class="text-subtitle-2 mt-1">MANUTENÇÃO PROGRAMADA: MELHORIAS NO SISTEMA</div>
              </div>
              <v-btn 
                color="grey" 
                size="small" 
                variant="tonal"
                class="ml-2 text-none"
              >
                MANUTENÇÃO
              </v-btn>
            </div>
          </v-card>
        </v-list-item>
      </v-list>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  name: 'NewsList'
}
</script>

<style scoped>
.news-list-card {
  border: 1px solid rgba(212, 175, 55, 0.3);
  background-color: #2A2A2A !important;
}
</style>
