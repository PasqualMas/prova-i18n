<template>
  <v-select :items="items" v-model="langSelected" :label="$t('select')">
    <template slot="item" slot-scope="data">
      <img :src="`https://www.countryflags.io/${getFlag(data.item)}/shiny/32.png`" class="mr-2" />
      {{data.item}}
    </template>
  </v-select>
</template>

<script>
export default {
  name: "locale-changer",
  created() {
    let langName = this.$i18n.locale === 'en' ? 'English' : 'Español'
    this.langSelected = langName
  },
  data() {
    return {
      langSelected: null,
      items: ["English", "Español"]
    };
  },
  methods: {
    getFlag(lang) {
      return lang === "English" ? "gb" : "es";
    }
  },
  watch: {
    langSelected(val) {
      let langCode = val === "English" ? "en" : "es";
      this.$i18n.locale = langCode;
    }
  }
};
</script>