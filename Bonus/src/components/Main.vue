<template>
  <main>
    <div class="container py-5">
      <CardsContainer></CardsContainer>
    </div>
  </main>
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
main {
  position: relative;
  width: 100%;

  background-color: #192d3b;
}
</style>