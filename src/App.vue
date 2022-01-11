<template>
  <Home />
</template>

<script>
import Home from "./components/Home.vue";

export default {
  name: "App",
  components: {
    Home,
  },
};
</script>

<style lang="css">
@import "./import-font.css";
:root {
  --secondary-font: "Cyberthrone";
  --main-font: "CreatoDisplay";
  --background-color: #fcf9ee;
  --main-color: #030611;
  --image-width: 32.5vw;
}
* {
  box-sizing: border-box;
  user-select: none;
}
body {
  margin: 0;
  background: var(--background-color);
  overflow-x: hidden;
}
html {
  background: var(--background-color);
}
body::-webkit-scrollbar {
  display: none;
}
#app {
  font-family: var(--main-font);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #030611;
}
</style>
