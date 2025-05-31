<template>
  <v-card class="mb-4 ranking-card">
    <v-card-title class="d-flex align-center">
      <v-icon :color="titleColor" class="mr-2">{{ titleIcon }}</v-icon>
      {{ title }}
    </v-card-title>
    <v-card-text class="pa-0">
      <v-list density="compact" bg-color="transparent">
        <v-list-item v-for="(player, index) in players" :key="index">
          <v-card variant="flat" color="grey-darken-4" class="w-100 pa-2 mb-2">
            <div class="d-flex align-center">
              <v-avatar size="30" :color="getClassColor(player.class)" class="mr-2">
                <span class="text-caption">{{ index + 1 }}</span>
              </v-avatar>
              <div>
                <div class="text-body-2">{{ player.name }}</div>
                <div class="text-caption">{{ player.class }}</div>
              </div>
              <v-spacer></v-spacer>
              <div class="text-h6" :class="getPointsColor(player.points)">{{ player.points }}</div>
            </div>
          </v-card>
        </v-list-item>
      </v-list>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  name: 'RankingCard',
  props: {
    title: {
      type: String,
      required: true
    },
    type: {
      type: String,
      default: 'semanal',
      validator: (value) => ['semanal', 'diario', 'mensal'].includes(value)
    }
  },
  computed: {
    titleIcon() {
      const icons = {
        'semanal': 'mdi-calendar-week',
        'diario': 'mdi-calendar-today',
        'mensal': 'mdi-calendar-month'
      };
      return icons[this.type] || 'mdi-trophy';
    },
    titleColor() {
      const colors = {
        'semanal': 'amber',
        'diario': 'orange',
        'mensal': 'deep-orange'
      };
      return colors[this.type] || 'primary';
    },
    players() {
      // Dados simulados para cada tipo de ranking
      if (this.title === 'TOP 5 SEMANAL') {
        return [
          { name: 'DRAGONSLAYER', class: 'MÁGICO • LEVEL 90', points: '15.420' },
          { name: 'ICEWARD', class: 'FROST • LEVEL 85', points: '14.890' },
          { name: 'FIREKNIGHT', class: 'EMBER • LEVEL 92', points: '14.650' },
          { name: 'SHADOWARCHER', class: 'VOID • LEVEL 78', points: '14.200' },
          { name: 'HOLYPALADIN', class: 'LIGHT • LEVEL 80', points: '13.980' }
        ];
      } else if (this.title === 'TOP 5 DIÁRIO') {
        return [
          { name: 'MYSTICMAGE', class: 'ARCANO • LEVEL 88', points: '2.840' },
          { name: 'BLOODWARRIOR', class: 'GUARDIÃO • LEVEL 95', points: '2.650' },
          { name: 'WINDRANGER', class: 'STORM • LEVEL 88', points: '2.480' },
          { name: 'EARTHSHAMAN', class: 'TERRA • LEVEL 75', points: '2.320' },
          { name: 'VOIDASSASSIN', class: 'SHADOW • LEVEL 89', points: '2.180' }
        ];
      } else if (this.title === 'TOP 5 MENSAL') {
        return [
          { name: 'LEGENDMASTER', class: 'ETERNAL • LEVEL 100', points: '58.900' },
          { name: 'CHAOSLORD', class: 'DARKNESS • LEVEL 98', points: '56.750' },
          { name: 'ANGELWING', class: 'HEAVEN • LEVEL 96', points: '54.200' },
          { name: 'DEMONBANE', class: 'SACRED • LEVEL 92', points: '52.800' },
          { name: 'RUNEMASTER', class: 'ANCIENT • LEVEL 95', points: '51.450' }
        ];
      }
      return [];
    }
  },
  methods: {
    getClassColor(classText) {
      if (classText.includes('MÁGICO') || classText.includes('ARCANO') || classText.includes('ETERNAL')) return 'purple';
      if (classText.includes('FROST') || classText.includes('DARKNESS')) return 'blue-grey';
      if (classText.includes('EMBER') || classText.includes('HEAVEN')) return 'orange';
      if (classText.includes('VOID') || classText.includes('SHADOW') || classText.includes('SACRED')) return 'deep-purple';
      if (classText.includes('LIGHT') || classText.includes('TERRA') || classText.includes('ANCIENT')) return 'teal';
      if (classText.includes('STORM') || classText.includes('GUARDIÃO')) return 'red';
      return 'grey';
    },
    getPointsColor(points) {
      if (parseInt(points.replace(/\./g, '')) > 50000) return 'primary--text';
      if (parseInt(points.replace(/\./g, '')) > 10000) return 'info--text';
      return 'warning--text';
    }
  }
}
</script>

<style scoped>
.ranking-card {
  border: 1px solid rgba(212, 175, 55, 0.3);
  background-color: #2A2A2A !important;
}
</style>
