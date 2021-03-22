<template>
  <header>
    <h1>{{ content }}</h1>
  </header>
</template>

<script>
export default {
  props: ["content"],
};
</script>
<style scoped>
/* * {
  margin: 0;
  padding: 0;
} */
h1 {
  background-color: orange;
  color: white;
  padding: 20px 0;
}
</style>
