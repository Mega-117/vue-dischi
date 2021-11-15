<template>
  <div>
    <div v-for="(item, i) in diskList" :key="i">
      {{ item.title }}
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