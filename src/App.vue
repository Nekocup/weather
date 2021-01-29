<template>
  <div id="app">
    <header>
      <h3>Weather</h3>
    </header>
    <div class="container">
      <nav>
        <nav-bar></nav-bar>
      </nav>
      <main>
        <main-container></main-container>
      </main>
    </div>
  </div>
</template>

<script>
import navBar from "@/components/nav-bar";
import mainContainer from "@/components/main-container";

export default {
  name: "app",
  components: {
    "nav-bar": navBar,
    "main-container": mainContainer,
  },
};
</script>

<style lang="scss">
body {
  min-height: 100vh;
  background-image: linear-gradient(
    109.6deg,
    rgba(253, 199, 141, 1) 11.3%,
    rgba(249, 143, 253, 1) 100.2%
  );
}
header {
  display: none;
}
@media screen AND (min-width: 1201px) {
  header {
    display: block;
    width: 100%;
    text-align: center;
    padding: 1em 0;
    box-shadow: 1px 1px 10px black;
    margin-bottom: 10px;
  }
  .container {
    display: flex;
  }
  nav {
    width: 25%;
  }
  main {
    width: 75%;
  }
}
</style>
