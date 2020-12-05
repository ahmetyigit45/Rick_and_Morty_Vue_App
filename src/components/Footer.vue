<template>
  <v-footer color="#385F73" padless>
    <v-card
      flat
      tile
      class="indigo lighten-1 white--text text-center"
      style="width:100%"
    >
      <v-card-text class="white--text" style="background:#385F73">
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
