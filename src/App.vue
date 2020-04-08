<template>
  <div id="app">
    <v-card>
      <HelloI18n/>
      <localeChanger></localeChanger>
    </v-card>
  </div>
</template>

<script>
import HelloI18n from "./components/HelloI18n";
import localeChanger from "./components/localeChanger"
export default {
  name: 'app',
  components: {
    HelloI18n,
    localeChanger
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>