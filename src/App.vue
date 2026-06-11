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
@import url('https://fonts.googleapis.com/css2?family=Lobster&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Amatic+SC&display=swap');
@import url("https://fonts.googleapis.com/css2?family=Faster+One&display=swap");
@import url('https://fonts.googleapis.com/css2?family=Google+Sans+Flex:opsz,wght@6..144,1..1000&display=swap');

.borderline {
  border-style: solid;
  border-radius: 1px;
  border-color: red;
}

#app {
  font-family: "Google Sans Flex", sans-serif;
  font-optical-sizing: auto;
  font-weight: <weight>;
  font-style: normal;
  font-variation-settings:
    "slnt" 0,
    "wdth" 100,
    "GRAD" 0,
    "ROND" 0;
}

.section {
  font-family: "Lobster", sans-serif;
  font-weight: 400;
  font-style: normal;
  color: cornflowerblue;
}

.name {
  font-family: "Faster One", cursive;
  font-weight: 400;
  font-style: normal;
  font-size: 35px;
  color: rgb(161, 167, 172);
}

.title {
  font-family: "Amatic SC", sans-serif;
  font-weight: 400;
  font-style: normal;
  font-size: 60px;
  color: cadetblue;
}
</style>
