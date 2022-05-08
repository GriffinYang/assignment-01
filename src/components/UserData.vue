<template>
  <ul class="data-container">
    <li>
      <label for="">Username:</label>
      <h2>{{ userName }}</h2>
      <label for="">Age:</label>
      <h3>{{ userAge }}</h3>
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    userName: {
      required: true,
      type: String,
    },
    userAge: {
      required: true,
      type: String,
    },
  },
};
</script>
