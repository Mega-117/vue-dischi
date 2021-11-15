<template>
  <Card></Card>
</template>

<script>
import Card from "./Card.vue";
import axios from "axios";

export default {
  name: "CardContainer",
  components: {
    Card,
  },
  mounted() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((respose) => {
        console.log(respose);
        debugger;
      });
  },
};
</script>

<style>
</style>