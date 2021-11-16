<template>
  <div>
    <select
      class="form-select mb-4 text-white"
      aria-label="Default select example"
    >
      <option selected>Open this select menu</option>
      <option value="1">One</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "DiskFilter",
};
</script>

<style>
.form-select {
  background-color: #2b3a46 !important;
  width: 225px !important;
}
</style>