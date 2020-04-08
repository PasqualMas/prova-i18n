<template>
  <v-container>
    <v-btn v-for="(lang, idx) in langs" 
           :key=idx
           @click="$i18n.locale = lang.str"
    >
    <v-icon left>{{lang.ico}}</v-icon>
      {{lang.str}}
      </v-btn>
  </v-container>
</template>

<script>  
export default {
  name: 'locale-changer',
  data () {
    return {
       dialog: null,
       langs: [
         {
           str: 'en',
           ico: '🇬🇧',
         },
         { 
           str: 'es',
           ico: '🇪🇸'
         }
         ]
        }
  }
}
</script>