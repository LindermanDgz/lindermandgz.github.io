<template>
  <v-app :theme="theme">
    <v-fab location="top end" :icon="icon" @click="toggleTheme" icon-color="red" absolute app appear></v-fab>
    <v-main>
      <Resume />
    </v-main>
  </v-app>
</template>

<script setup>
  import Resume from '@/components/Resume.vue'
</script>


<script>
export default {
  data() {
    return {
      theme: 'dark',
      icon: 'mdi-white-balance-sunny',
    }
  },
  methods: {
    toggleTheme() {
      this.theme = this.theme === 'light' ? 'dark' : 'light';
      this.icon = this.theme === 'light' ? 'mdi-weather-night' : 'mdi-white-balance-sunny'
    }
  }
}
</script>

<style>
/* @import url('https://fonts.googleapis.com/css2?family=Nabla&display=swap'); */
@import url('https://fonts.googleapis.com/css2?family=Bungee+Tint&family=Nabla&display=swap');
/* @import url('https://fonts.googleapis.com/css2?family=Sixtyfour+Convergence&display=swap'); */

/*
.nabla-title {
  font-family: "Nabla", serif;
  font-optical-sizing: auto;
  font-weight: 400;
  font-style: normal;
  font-variation-settings:
    "EDPT" 100,
    "EHLT" 12;
} */

.bungee-tint-regular {
  font-family: "Bungee Tint", serif;
  font-weight: 400;
  font-style: normal;
}

/* .sixtyfour-convergence-title {
  font-family: "Sixtyfour Convergence", serif;
  font-optical-sizing: auto;
  font-weight: 400;
  font-style: normal;
  font-variation-settings:
    "BLED" 0,
    "SCAN" 0,
    "XELA" 0,
    "YELA" 0;
} */

.borderline {
  border-style: solid;
  border-radius: 1px;
  border-color: red;
}
</style>
