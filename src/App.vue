<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style lang="scss">
@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.13.0/css/all.min.css");
@import url("https://fonts.googleapis.com/css2?family=Prompt:wght@500&display=swap");

* {
  font-family: "Prompt", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

.container {
  width: 85vw;
  margin: auto;
}

h1 {
  color: #694b64;
  text-align: left;
  font-family: Georgia, "Times New Roman", Times, serif;
}
</style>
