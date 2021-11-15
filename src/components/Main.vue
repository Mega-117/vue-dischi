<template>
  <div class="bg-main">
    <div class="container">
      <div class="row row-cols-5">
        <CardsContainer></CardsContainer>
      </div>
    </div>
  </div>
</template>

<script>
import CardsContainer from "./CardsContainer.vue";

export default {
  name: "Main",
  components: {
    CardsContainer,
  },
};
</script>

<style>
.bg-main {
  background-color: #192d3b;
  height: calc(100vh - 70px);
}
</style>