<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          v-bind:src="logo"
          transition="scale-transition"
          width="40"
        />
        <h1>Developer Dashboard</h1>
      </div>

      <v-spacer></v-spacer>
    </v-app-bar>

    <v-content>
      <router-view/>
    </v-content>
  </v-app>
</template>

<script>
var logo = "https://www.okta.com/sites/all/themes/Okta/images/logos/developer/Dev_Logo-03_White_Large.png"
if(process.env.VUE_APP_LOGO) {
  logo = process.env.VUE_APP_LOGO
}

export default {
  name: 'App',

  data: () => ({
    logo: logo
  }),
};
</script>
