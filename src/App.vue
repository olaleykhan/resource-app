<template>
  <div>
    <the-header content="Programming Learning Resouces"></the-header>
    <the-resources> </the-resources>
    <remove-tab>
      <hr />
      <br />
      <h1>remove</h1>
      <hr />
    </remove-tab>
  </div>
</template>

<script>
import TheResources from "./components/learning-resources/TheResources";
// import TheHeader from "./layouts/TheHeader";
import TheHeader from "./layouts/TheHeader.vue";
import RemoveTab from "./components/RemoveTab";

export default {
  name: "App",
  components: {
    TheResources,
    TheHeader,
    RemoveTab,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body,
html {
  padding: 0;
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}
a {
  text-decoration: none;
  color: orange;
  /* color: greenyellow; */
}
li {
  list-style-type: none;
}
</style>
