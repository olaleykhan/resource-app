<template>
  <ul>
    <display-resource
      v-for="resource in resources"
      :key="resource.id"
      :title="resource.title"
      :link="resource.link"
      :description="resource.description"
    >
    </display-resource>
    <!-- <li v-for="resource in storedResources" :key="resource.id">
      {{ resource }}
    </li> -->
  </ul>
</template>

<script>
import DisplayResource from "./DisplayResource";
export default {
  props: ["resources"],
  name: "DisplayResources",
  components: {
    DisplayResource,
  },
};
</script>

<style scoped>
ul {
  list-style: none;
  margin: 0;
  padding: 0;
  margin: auto;
  max-width: 40rem;
}
</style>
