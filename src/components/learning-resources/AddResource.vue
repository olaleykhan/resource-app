<template>
  <base-card>
    <form @submit="submitForm">
      <div class="form-control">
        <label for="title">Title</label>
        <input type="text" id="title" name="title" ref="inputTitle" />
      </div>
      <div class="form-control">
        <label for="description">Description</label>
        <!-- <input type="text" id="title" name="title"> -->
        <textarea
          name="Description"
          id="description"
          cols="50"
          rows="3"
          ref="inputDescription"
        ></textarea>
      </div>
      <div class="form-control">
        <label for="link">Link</label>
        <input type="url" id="link" name="link" ref="inputLink" />
      </div>
      <div>
        <base-button type="submit"> Submit form</base-button>
      </div>
    </form>
  </base-card>
</template>
<script>
export default {
  name: "AddResource",
  inject: ["addResourceData"],
  methods: {
    submitForm(e) {
      // let title = ;
      e.preventDefault();
      const title = this.$refs.inputTitle.value;
      const description = this.$refs.inputDescription.value;
      const link = this.$refs.inputLink.value;
      const newResource = {
        title,
        description,
        link,
      };
      this.addResourceData(newResource);
      console.log(newResource);
      this.$refs.inputTitle.value = "";
      this.$refs.inputDescription.value = "";
      this.$refs.inputLink.value = "";
    },
  },
};
</script>

<style scoped>
label {
  font-weight: bold;
  display: block;
  margin-bottom: 0.5rem;
}

input,
textarea {
  display: block;
  width: 100%;
  font: inherit;
  padding: 0.15rem;
  border: 1px solid #ccc;
}

input:focus,
textarea:focus {
  outline: none;
  border-color: #3a0061;
  background-color: #f7ebff;
}

.form-control {
  margin: 1rem 0;
}
</style>
