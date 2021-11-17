<template>
  <div>
    <select
      v-model="genereMusicale"
      @change="$emit('searchGenre', genereMusicale)"
      class="form-select mb-4 text-white"
      aria-label="Default select example"
    >
      <option selected>Open this select menu</option>
      <option :value="elemeto" v-for="(elemeto, i) in arrGeneri" :key="i">
        {{ elemeto }}
      </option>
    </select>
  </div>
</template>

<script>
export default {
  name: "DiskFilter",
  props: ["arrGeneri"],
  data() {
    return {
      genereMusicale: "",
    };
  },
};
</script>

<style>
.form-select {
  background-color: #2b3a46 !important;
  width: 225px !important;
}
</style>