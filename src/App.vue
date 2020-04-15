<template>
  <v-app>
    <v-card width="400" class="pa-4" style="margin: auto">
      <v-row>
        <v-col cols="8">
          <v-card-title>{{ $t('hello') }}</v-card-title>
        </v-col>
        <v-col cols="4">
          <localeChanger></localeChanger>
        </v-col>
      </v-row>
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