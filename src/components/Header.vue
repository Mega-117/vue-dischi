<template>
  <header>
    <nav class="py-2 px-4">
      <img
        src="https://upload.wikimedia.org/wikipedia/commons/7/75/Spotify_icon.png"
        alt="logo-spotyfy"
      />
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped lang="scss">
nav {
  background-color: #2b3a46;
  height: 70px;

  img {
    height: 100%;
  }
}
</style>