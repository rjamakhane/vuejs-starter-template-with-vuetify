<template>
  <v-navigation-drawer
    v-model="drawer"
    :color="color"
    :expand-on-hover="expandOnHover"
    :mini-variant="miniVariant"
    :right="right"
    :fixed="fixed"
    :clipped="clipped"
    dark
    app
  >
    <v-list dense nav class="py-0">
      <v-list-item two-line :class="miniVariant && 'px-0'">
        <v-list-item-avatar>
          <img
            src="https://media-exp1.licdn.com/dms/image/C5103AQEr3q_1PuVhuA/profile-displayphoto-shrink_200_200/0?e=1592438400&v=beta&t=lpw-2-fUFpO49X8FEc9H2ok8dD8H0b1lIiNPVtvguXU"
          />
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title>Application</v-list-item-title>
          <v-list-item-subtitle>Subtext</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list-item v-for="item in items" :key="item.title" :to="{name:item.title}" activeClass="active">
        <v-list-item-icon>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  props: {
    miniVariant: Boolean
  },
  data: () => ({
    drawer: true,
    items: [
      {
        title: "Home",
        icon: "mdi-view-dashboard"
      },
      {
        title: "About",
        icon: "mdi-account"
      },
      {
        title: "Contact",
        icon: "mdi-cloud-circle",
      }
    ],
    color: "success",
    colors: ["primary", "blue", "success", "red", "teal"],
    right: false,
    expandOnHover: false,
    background: false,
    fixed: true,
    clipped: true
  })
};
</script>

<style>
</style>
