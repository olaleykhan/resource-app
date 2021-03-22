<template>
  <div>
    <slot> </slot>
  </div>
</template>

<script>
// import { defineComponent } from '@vue/composition-api'

export default {
  name: "BaseCard",
};
</script>

<style scoped>
div {
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  padding: 1rem;
  margin: 2rem auto;
  max-width: 40rem;
  /* min-height: 150px; */
  /* display: flex;
  flex-direction: column;
  justify-content: space-between; */
}
</style>
