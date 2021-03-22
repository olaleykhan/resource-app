<template>
  <div>
    <display-resources :resources="storedResources"> </display-resources>
  </div>
</template>

<script>
import DisplayResources from "./components/DisplayResources";
export default {
  name: "App",
  components: {
    DisplayResources,
  },
  data() {
    return {
      storedResources: [
        {
          id: "vue-site",
          title: " Vue resource",
          description: "Official guide of the vue people",
          link: "www.vuejs.org",
        },
        {
          id: "google-site",
          title: " Google resource",
          description: "search stuff on google",
          link: "www.google.com",
        },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
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
