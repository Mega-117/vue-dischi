<template>
  <div>
    <Loader v-if="loaderStatus === true"></Loader>
    <DiskFilter :arrGeneri="arrGeneri" @searchGenre="filterGenre"></DiskFilter>
    <div class="row row-cols-1 row-cols-md-5 g-4">
      <div class="col" v-for="(item, i) in filterGenre" :key="i">
        <Card
          :poster="item.poster"
          :title="item.title"
          :author="item.author"
          :year="item.year"
          :genre="item.genre"
        ></Card>
      </div>
    </div>
  </div>
</template>

<script>
import Card from "./Card.vue";
import axios from "axios";
import Loader from "./Loader.vue";
import DiskFilter from "./DiskFilter.vue";

export default {
  name: "CardContainer",
  components: {
    Card,
    Loader,
    DiskFilter,
  },
  data() {
    return {
      diskList: [],
      loaderStatus: true,
      arrGeneri: [],
      arrFiltrato: [],
    };
  },
  methods: {
    filterGenre(genereSelezionato) {
      console.log(genereSelezionato);
      if (!genereSelezionato) {
        return this.diskList;
      }
      this.diskList.filter((disco) => {
        return disco.genre === genereSelezionato;
      });
    },
  },
  computed: {},
  mounted() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((rispotaAxios) => {
        this.diskList = rispotaAxios.data.response;
        setTimeout(() => {
          this.loaderStatus = false;
        }, 1000);
        for (let i = 0; i < this.diskList.length; i++) {
          let element = this.diskList[i].genre;
          if (!this.arrGeneri.includes(element)) {
            this.arrGeneri.push(element);
          }
        }
      });
  },
};
</script>

<style>
.form-select {
  background-color: #2b3a46;
  width: 225px;
}
</style>