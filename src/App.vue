<template>
  <v-app :theme="theme">
    <v-app-bar app dark elevation="4" class="app-header">
      <div class="d-flex align-center">
        <div class="logo-container">
          <v-icon icon="mdi-crown" color="primary" size="large" class="mr-2"></v-icon>
          <span class="text-h5 font-weight-bold primary--text">OO Online</span>
        </div>
        <span class="text-caption text-uppercase ml-1">Kingdom of Adventure</span>
      </div>
      <v-spacer></v-spacer>
      <v-btn class="mx-1 text-none" variant="text" color="primary">
        <v-icon left>mdi-home</v-icon>
        Início
      </v-btn>
      <v-btn class="mx-1 text-none" variant="text" color="primary">
        <v-icon left>mdi-account-plus</v-icon>
        Cadastro
      </v-btn>
      <v-btn class="mx-1 text-none" variant="text" color="primary">
        <v-icon left>mdi-download</v-icon>
        Downloads
      </v-btn>
    </v-app-bar>

    <v-main>
      <v-container fluid class="pa-0">
        <!-- Banner Principal -->
        <div class="banner-container">
          <div class="banner-content">
            <h1 class="text-h2 font-weight-bold primary--text text-center">Reino Épico</h1>
            <p class="text-subtitle-1 text-center">A MAIOR AVENTURA MMORPG MEDIEVAL TE ESPERA</p>
          </div>
        </div>

        <!-- Conteúdo Principal -->
        <v-container>
          <v-row>
            <!-- Coluna Esquerda -->
            <v-col cols="12" md="8">
              <!-- Servidor Principal -->
              <server-status />

              <!-- Informações do Jogo -->
              <game-info />

              <!-- Castle Siege -->
              <castle-siege />

              <!-- Últimas Notícias -->
              <news-list />
            </v-col>

            <!-- Coluna Direita -->
            <v-col cols="12" md="4">
              <!-- Dados do Servidor -->
              <server-data />

              <!-- Rankings -->
              <ranking-card title="TOP 5 DIÁRIO" />
              <ranking-card title="TOP 5 SEMANAL" />
              <ranking-card title="TOP 5 MENSAL" />

              <!-- Equipe -->
              <team-list />
            </v-col>
          </v-row>
        </v-container>
      </v-container>
    </v-main>

    <v-footer dark class="pa-4">
      <v-row>
        <v-col cols="12" md="4" class="d-flex align-center">
          <v-icon icon="mdi-crown" color="primary" size="large" class="mr-2"></v-icon>
          <span class="text-h6 font-weight-bold primary--text">OO Online</span>
        </v-col>
        <v-col cols="12" md="4">
          <div class="text-center">
            <div class="text-subtitle-2 mb-2">LINKS RÁPIDOS</div>
            <v-btn variant="text" color="primary" class="mx-1 text-none">INÍCIO</v-btn>
            <v-btn variant="text" color="primary" class="mx-1 text-none">CADASTRO</v-btn>
            <v-btn variant="text" color="primary" class="mx-1 text-none">DOWNLOADS</v-btn>
          </div>
        </v-col>
        <v-col cols="12" md="4">
          <div class="text-center">
            <div class="text-subtitle-2 mb-2">COMUNIDADE</div>
            <v-btn icon color="primary" class="mx-1">
              <v-icon>mdi-facebook</v-icon>
            </v-btn>
            <v-btn icon color="primary" class="mx-1">
              <v-icon>mdi-discord</v-icon>
            </v-btn>
            <v-btn icon color="primary" class="mx-1">
              <v-icon>mdi-twitter</v-icon>
            </v-btn>
          </div>
        </v-col>
        <v-col cols="12" class="text-center mt-4">
          <span class="text-caption">© 2024 MU ONLINE KINGDOM. TODOS OS DIREITOS RESERVADOS. FORJADO COM MAGIA E
            CÓDIGO</span>
        </v-col>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'App',
  setup() {
    const theme = ref('dark')

    return {
      theme
    }
  }
}
</script>

<style>
* {
  font-family: 'Cinzel', serif;
}

.app-header {
  background-color: #1E1E1E !important;
  border-bottom: 1px solid #D4AF37;
}

.logo-container {
  display: flex;
  align-items: center;
}

.banner-container {
  background-image: url('@/assets/images/banner-background.png');
  background-size: cover;
  background-position: center;
  height: 300px;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
}

.banner-container::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
}

.banner-content {
  position: relative;
  z-index: 1;
  padding: 2rem;
  text-align: center;
}

.banner-content h1 {
  font-family: 'Cinzel Decorative', serif;
  text-shadow: 0 0 10px rgba(212, 175, 55, 0.7);
  border: 2px solid #D4AF37;
  display: inline-block;
  padding: 0.5rem 2rem;
}

.banner-content p {
  font-family: 'Cinzel', serif;
  margin-top: 1rem;
}

/* Estilos globais */
h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: 'Cinzel', serif;
}

.v-card {
  border: 1px solid rgba(212, 175, 55, 0.3);
  background-color: #2A2A2A !important;
}

.v-card-title {
  border-bottom: 1px solid rgba(212, 175, 55, 0.3);
  background-color: rgba(30, 30, 30, 0.8);
}

.card-title {
  color: #d4af37;
  font-size: 1rem;
}
</style>
