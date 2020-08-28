<template>
  <v-speed-dial absolute bottom right>
    <template v-slot:activator>
      <v-btn fab v-bind:color="color" @click="onClick">
        <v-icon>mdi-plus</v-icon>
      </v-btn>
    </template>
  </v-speed-dial>
</template>

<script>
export default {
  props: {
    onClick: {
      type: Function,
      default: () => {},
    },
    color: {
      type: String,
      default: "primary",
    },
  },
};
</script>
