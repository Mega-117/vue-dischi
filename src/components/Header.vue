<template>
  <header>
    <nav class="px-4 py-2">
      <div class="logo-container">
        <img
          src="https://upload.wikimedia.org/wikipedia/commons/7/75/Spotify_icon.png"
          alt="logo-spotyfy"
        />
      </div>
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
  .logo-container {
    width: 50px;
    height: 50px;
    img {
      height: 100%;
    }
  }
}
</style>