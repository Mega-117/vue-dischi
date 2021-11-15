<template>
  <div>
    <Loader v-if="loaderStatus === true"></Loader>
    <div class="row row-cols-1 row-cols-md-5 g-4">
      <div class="col" v-for="(item, i) in diskList" :key="i">
        <Card
          :poster="item.poster"
          :title="item.title"
          :author="item.author"
          :year="item.year"
        ></Card>
      </div>
    </div>
  </div>
</template>

<script>
import Card from "./Card.vue";
import axios from "axios";
import Loader from "./Loader.vue";

export default {
  name: "CardContainer",
  components: {
    Card,
    Loader,
  },
  data() {
    return {
      diskList: [],
      loaderStatus: true,
    };
  },
  mounted() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((rispotaAxios) => {
        this.diskList = rispotaAxios.data.response;
        setTimeout(() => {
          this.loaderStatus = false;
        }, 1000);
      });
  },
};
</script>

<style>
</style>