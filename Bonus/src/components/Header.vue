<template>
  <header>
    <nav class="px-4 py-2">
      <a href="#">
        <img
          src="https://upload.wikimedia.org/wikipedia/commons/7/75/Spotify_icon.png"
          alt="logo-spotyfy"
        />
      </a>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped lang="scss">
header {
  margin-bottom: 70px;
  nav {
    background-color: #2b3a46;
    height: 70px;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 10;

    img {
      height: 100%;
    }
  }
}
</style>