<template>
  <v-select :items="items" 
            v-model="languageSelected"
            @change="$i18n.locale = languageSelected"
            :label="$t('select')">
    </v-select>
</template>

<script>
export default {
  name: "locale-changer",
  data() {
    return {
      languageSelected: null,
      langs: [
        {
          str: "en",
          ico: "🇬🇧"
        },
        {
          str: "es",
          ico: "🇪🇸"
        }
      ]
    };
  },
  computed: {
    items() {
      let arr = this.langs.map(obj => {
        return obj.str;
      });
      return arr;
    }
  },
};
</script>