<template>
  <div>
    <div>
      <div class="row row-cols-1 row-cols-md-5 g-4">
        <div class="col" v-for="(item, i) in diskList" :key="i">
          <div class="card">
            <img
              src="https://upload.wikimedia.org/wikipedia/commons/7/75/Spotify_icon.png"
              class="card-img-top"
              alt="ciao"
            />
            <div class="card-body">
              <h5 class="card-title">Card title</h5>
              <p class="card-text">testo</p>
            </div>
          </div>
        </div>
      </div>
      <Card></Card>
    </div>
  </div>
</template>

<script>
import Card from "./Card.vue";
import axios from "axios";

export default {
  name: "CardContainer",
  components: {
    Card,
  },
  data() {
    return {
      diskList: [],
    };
  },
  mounted() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((rispotaAxios) => {
        this.diskList = rispotaAxios.data.response;
      });
  },
};
</script>

<style>
</style>