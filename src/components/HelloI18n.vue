<template>
    <v-container>
      <v-card-title>{{ $t('hello') }}</v-card-title>
      <v-card-title>{{ $t('welcome') }}</v-card-title>
      <v-btn>{{ $t('yes-button') }}</v-btn>
      <v-btn>{{ $t('no-button') }}</v-btn>
    </v-container>
</template>


<script>
export default {
  name: 'HelloI18n'
}
</script>

