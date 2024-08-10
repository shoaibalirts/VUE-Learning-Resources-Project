<template>
  <h2>Add Resource</h2>
  <!-- <base-card>
    <form>
      <div>
        <label>Title</label>
        <input type="text" v-model="enteredTitle" />
      </div>
      <div>
        <label>Description</label>
        <textarea cols="3" rows="3" v-model="enteredDescription"></textarea>
      </div>
      <div>
        <label>Link</label>
        <input type="text" v-model="enteredLink" />
      </div>
      <base-button type="submit">Submit</base-button>
    </form>
  </base-card> -->
</template>

<script>
export default {
  data() {
    return {
      enteredTitle: '',
      enteredDescription: '',
      enteredLink: '',
    };
  },
  methods: {
    addResource(event) {
      event.preventDefault();
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
