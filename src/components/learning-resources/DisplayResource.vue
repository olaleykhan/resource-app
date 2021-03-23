<template>
  <li>
    <base-card>
      <header>
        <h3>{{ title }}</h3>
        <base-button mode="flat">Delete</base-button>
      </header>

      <p>{{ description }}</p>
      <nav>
        <a :href="link" target="_blank">View Resource </a>
      </nav>
    </base-card>
  </li>
</template>

<script>
export default {
  name: "DisplayResource",
  props: ["link", "title", "description"],
  data() {
    return {
      a: null,
    };
  },
};
</script>

<style scoped>
header {
  display: flex;
  text-align: center;
  text-decoration: none;
  justify-content: space-around;
  width: 70%;
  margin: 0 auto;
  align-items: center;
}
/* button {
  outline: none;
  padding: 4px 10px;
  border: none;
  border-radius: 5px;
  height: fit-content;
  width: 5rem;
}
button:hover {
  background-color: orange;
  color: white;
  cursor: pointer;
  font-size: 1em;
  font-weight: bold;
} */
</style>
