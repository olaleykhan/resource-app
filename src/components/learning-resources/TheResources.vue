<template>
  <div>
    <base-card class="base-card">
      <base-button
        @click="changeSelectedTab('add-resource')"
        :mode="makeAddActive"
      >
        Add Resource
      </base-button>
      <base-button
        @click="changeSelectedTab('display-resources')"
        :mode="makeDisplayActive"
      >
        Display Stored Resources
      </base-button>
    </base-card>
    <!-- <display-resources :resources="resources"></display-resources>
    <add-resource></add-resource> -->
    <keep-alive>
      <component :is="selectedTab" v-bind="passResourceProp"></component>
    </keep-alive>
  </div>
</template>

<script>
import DisplayResources from "./DisplayResources";
import AddResource from "./AddResource.vue";
// import DisplayResources from "./components/learning-resources/DisplayResources";
export default {
  name: "TheResources",
  components: {
    DisplayResources,
    AddResource,
  },
  //   props: ["resources"],
  data() {
    return {
      selectedTab: "add-resource",
      storedResources: [
        {
          id: "vue-site",
          title: " Vue resource",
          description: "Official guide of the vue people",
          link: "https://www.vuejs.org",
        },
        {
          id: "google-site",
          title: " Google resource",
          description: "search stuff on google",
          link: "https://www.google.com/",
        },
      ],
    };
  },
  provide() {
    return {
      resources: this.storedResources,
      addResourceData: this.addResourceData,
    };
  },
  methods: {
    changeSelectedTab(tabName) {
      console.log(tabName);
      this.selectedTab = tabName;
    },
    addResourceData(obj) {
      this.storedResources.push(obj);
      this.selectedTab = "display-resources";
    },
  },
  computed: {
    passResourceProp() {
      if (this.selectedTab === "display-resources") {
        return { resources: "resources" };
      } else return null;
    },
    makeAddActive() {
      if (this.selectedTab === "add-resource") {
        return null;
      } else return "flat";
    },
    makeDisplayActive() {
      if (this.selectedTab === "display-resources") {
        return null;
      } else return "flat";
    },
  },
};
</script>

<style scoped>
.base-card {
  display: flex;
  justify-content: space-around;
  /* background-color: brown; */
}
</style>
