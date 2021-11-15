<template>
  <div>
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