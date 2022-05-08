<template>
  <div class="form-container">
    <form action="#">
      <h2>Add user data</h2>
      <label for="name">Name:</label>
      <input type="text" name="name" v-model="name" /><br />
      <label for="age">Age:</label>
      <input type="text" name="age" v-model="age" /><br />
      <button type="submit" @click.prevent="submitForm">Submit</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      age: '',
    };
  },
  methods: {
    submitForm() {
      this.$emit('setUserData', this.name, this.age);
    },
  },
};
</script>
