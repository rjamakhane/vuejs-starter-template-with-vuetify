<template>
  <v-app id="inspire">
    <app-navigation :miniVariant="miniVariant"></app-navigation>
    <app-header :updateMiniVariant="updateMiniVariant"></app-header>

    <v-content>
     <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
import Navigation from "./components/Navigation/Navigation.vue";
import Header from "./components/Header/Header.vue";
export default {
  props: {
    source: String
  },
  data: () => ({
    miniVariant: true
  }),
  methods :{
    updateMiniVariant(){
      return this.miniVariant = !this.miniVariant;
    }
  },
  created() {
    this.$vuetify.theme.dark = false;
  },
  components: {
    appNavigation: Navigation,
    appHeader : Header
  }
};
</script>

<style scoped>
.my-drawer {
  padding-top: 48px;
}
</style>
