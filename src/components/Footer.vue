<template>
  <v-footer color="primary" padless>
    <v-card
      flat
      tile
      class="indigo lighten-1 white--text text-center"
      style="width:100%"
      color="primary"
    >
      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Ahmet YİĞİT</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>
