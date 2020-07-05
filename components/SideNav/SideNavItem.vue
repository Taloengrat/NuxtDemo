<template>
  <v-card class="ms-3 mb-2 pa-3 btnTest" style="start">
    <v-icon left>{{ icon }}</v-icon
    >{{ label }}
  </v-card>
</template>

<script>
export default {
  props: {
    icon: {
      type: String,
      default: 'mdi-account',
    },
    label: {
      type: String,
      default: 'Undefined',
    },
  },
}
</script>
