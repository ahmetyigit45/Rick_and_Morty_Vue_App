<template>
  <div class="main-wrapper" style="background:#FFFFFF ; height:100%">
    <v-container fluid>
      <v-row>
        <!--  <v-col md="4"> -->
        <v-col md="4" v-for="(item, index) in data" :key="index">
          <v-card
            class="mx-auto wrapper-card"
            color="primary"
            dark
            @click="goEpisodeDetail(item.url)"
          >
            <v-card-text>
              <div>{{ item.episode }}</div>
              <p class="display-1 text--primary text-wrapper">
                {{ item.name }}
              </p>
              <p>{{ item.air_date }}</p>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
      <v-row>
        <v-col class="text-center">
          <v-btn class="mx-2" fab dark medium color="primary" @click="prev">
            <v-icon dark>
              mdi-arrow-left
            </v-icon>
          </v-btn>
          <v-btn class="mx-2" fab dark medium color="primary" @click="next">
            <v-icon dark>
              mdi-arrow-right
            </v-icon>
          </v-btn>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      data: [],
      info: [],
      nextUrl: null,
      prevUrl: null,
      currentPage: "https://rickandmortyapi.com/api/episode",
    };
  },
  methods: {
    goEpisodeDetail(row) {
      this.$router.push({
        name: "Episodes",
        params: { episodeDetail: row },
      });
    },
    prev() {
      this.currentPage = this.info.prev;
      this.getItems();
    },
    next() {
      this.currentPage = this.info.next;
      this.getItems();
    },
    getItems() {
      axios.get(`${this.currentPage}`).then((response) => {
        this.info = response.data.info;
        this.data = response.data.results;
      });
    },
  },
  created() {
    this.getItems();
  },
};
</script>

<style lang="scss" scoped>
.wrapper-card {
  height: 100%;
  width: 100%;
}
.text-wrapper {
  width: 100%;
  white-space: nowrap;
  text-overflow: ellipsis;
  overflow: hidden;
}
</style>
