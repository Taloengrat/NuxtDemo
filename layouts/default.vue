<template>
  <v-app>
    <v-app-bar fixed app>
      <v-icon large color="primary">mdi-home</v-icon>
      <v-text-field
        class="ms-3"
        hide-details
        outlined
        placeholder="Search"
        prepend-inner-icon="mdi-magnify"
        clearable
        >Search</v-text-field
      >
      <v-spacer></v-spacer>
      <v-tabs centered>
        <v-tab><v-icon>mdi-home</v-icon></v-tab>
        <v-tab><v-icon>mdi-television</v-icon></v-tab>
        <v-tab><v-icon>mdi-shopping</v-icon></v-tab>
        <v-tab><v-icon>mdi-account-group</v-icon></v-tab>
        <v-tab><v-icon>mdi-gamepad-variant</v-icon></v-tab>
      </v-tabs>

      <v-spacer></v-spacer>

      <v-btn>Profile</v-btn>
      <v-btn color="primary" fab small dark class="ms-2">
        <v-icon>mdi-plus</v-icon>
      </v-btn>
      <v-btn color="primary" fab small dark class="ms-2">
        <v-icon>mdi-forum</v-icon>
      </v-btn>
      <v-btn color="primary" fab small dark class="ms-2">
        <v-icon>mdi-bell</v-icon>
      </v-btn>
      <v-btn color="primary" fab small dark class="ms-2">
        <v-icon>mdi-menu-down</v-icon>
      </v-btn>
    </v-app-bar>

    <v-content>
      <nuxt />
    </v-content>

    <v-footer :absolute="!fixed" color="gray" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,

      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
    }
  },
}
</script>
