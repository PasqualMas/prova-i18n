<template>
  <v-app>
    <v-card max-width="400" class="pa-4" style="margin: auto">
      <v-card-title>{{ $t('hello') }}</v-card-title>
      <localeChanger></localeChanger>
    </v-card>
  </v-app>
</template>

<script>
import localeChanger from "./components/localeChanger";
export default {
  name: "app",
  components: {
    localeChanger
  },
  data: () => ({
    items: ["Foo", "Bar", "Fizz", "Buzz"]
  }) 
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>