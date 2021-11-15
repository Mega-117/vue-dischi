<template>
  <div>
    <div class="card text-center px-3 pt-3 pb-0 my-card">
      <img :src="poster" class="card-img-top" alt="ciao" />
      <div class="card-body px-3 pt-3 pb-0">
        <h5 class="card-title text-white">{{ title }}</h5>
        <p class="card-text mb-0">{{ author }}</p>
        <p class="card-text">{{ year }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    poster: String,
    title: String,
    author: String,
    year: String,
  },
};
</script>

<style lang="scss">
.my-card {
  min-height: 360px;
  background-color: #2b3a46 !important;
  p {
    color: #808080;
  }
}
</style>