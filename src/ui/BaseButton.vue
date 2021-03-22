<template>
  <button :class="mode">
    <slot> </slot>
  </button>
</template>

<script>
export default {
  props: ["mode"],
  name: "BaseButton",
};
</script>

<style scoped>
button {
  padding: 0.5rem 1.5rem;
  background-color: orange;
  border-radius: 8px;
  outline: none;
  border: 1px solid transparent;
  color: white;
}

button:hover {
  background-color: white;
  color: orange;
  border: 1px solid orange;
  cursor: pointer;
}

.flat {
  background-color: inherit;
  color: black;
}
.flat:hover {
  background-color: none;
  border: 1px solid rgba(231, 224, 224);
  color: rgba(231, 224, 224);
}
</style>
