<template>
  <v-row justify="space-between">
    <v-col>
      <side-nav-item icon="mdi-account" :label="fullName"> </side-nav-item>
      <side-nav-item
        v-for="i in sideNavMenu"
        :key="i.label"
        :icon="i.icon"
        :label="i.label"
      >
      </side-nav-item>
    </v-col>

    <v-spacer></v-spacer>
    <v-col>
      <v-card color="pink" class="text-center">
        <v-btn outlined color="white">{{ firstName }} {{ lastName }}</v-btn>
      </v-card>
    </v-col>
    <v-spacer></v-spacer>
    <v-col>
      <v-card color="pink" class="me-3 text-right">
        <v-btn outlined color="white">{{ firstName }} {{ lastName }}</v-btn>
      </v-card>
    </v-col>
  </v-row>

  <!-- <v-row justify="center">
      <v-btn outlined color="white">{{ firstName }} {{ lastName }}</v-btn>
    </v-row> -->
</template>

<script>
import SideNavItem from '@/components/SideNav/SideNavItem'
export default {
  components: {
    SideNavItem,
  },
  data() {
    return {
      firstName: 'Taloengrat',
      lastName: 'poomchaiya',
      sideNavMenu: [
        { icon: 'mdi-account-multiple', label: 'Friends' },
        { icon: 'mdi-message', label: 'Messenger' },
        { icon: 'mdi-flag', label: 'Pages' },
        { icon: 'mdi-shopping', label: 'Market Place' },
        { icon: 'mdi-menu-down', label: 'See More' },
      ],
    }
  },
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`
    },
  },
}
</script>

<style>
.btnTest:hover {
  background-color: skyblue;
}
</style>
