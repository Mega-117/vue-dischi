<template>
  <div>
    <div class="bg-loader">
      <button class="btn btn-light" type="button" disabled>
        <span
          class="spinner-border spinner-border-sm"
          role="status"
          aria-hidden="true"
        ></span>
        <span class="sr-only" ps-1> Loading...</span>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Loader",
};
</script>

<style lang="scss">
.bg-loader {
  width: 100%;
  height: 100%;
  position: fixed;
  top: 70px;
  left: 0;
  z-index: 30;
  background-color: #192d3b;
  .btn {
    position: fixed;
    z-index: 2;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 20px;
  }
}
</style>