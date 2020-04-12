<template>
  <v-app-bar app clipped-left color="success" dense>
    <v-app-bar-nav-icon @click.stop="updateMiniVariant" />
    <v-icon class="mx-4" large>mdi-weather-hazy</v-icon>
    <v-toolbar-title class="mr-12 align-center">
      <span class="title">Demo</span>
    </v-toolbar-title>
    <v-spacer />
  </v-app-bar>
</template>

<script>
export default {
    props :{
        updateMiniVariant: Function
    }
};
</script>

<style>
</style>