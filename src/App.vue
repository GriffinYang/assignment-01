<template>
  <ul>
    <active-user @setUserData="setData"></active-user>
    <user-data
      v-for="user in users"
      :key="user.name"
      :user-name="user.name"
      :user-age="user.age"
    ></user-data>
  </ul>
</template>
<script>
export default {
  data() {
    return {
      users: [
        {
          name: 'Griffin Yang',
          age: '22',
        },
      ],
    };
  },
  methods: {
    setData(userName, userAge) {
      const currentUser = {};
      currentUser.name = userName;
      currentUser.age = userAge;
      this.users.push(currentUser);
    },
  },
};
</script>
<style>
#app label {
  font-size: 1rem;
  font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
  width: 50px;
  display: inline-block;
  font-weight: bold;
  color: #5c116b;
}
#app h2 {
  color: #194d35;
  font-family: 'Trebuchet MS';
}
#app form,
.data-container {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 1rem auto;
  border-radius: 10px;
  padding: 1rem;
  text-align: center;
  width: 90%;
  max-width: 40rem;
}
#app .form-container {
  display: flex;
  justify-content: center;
}
#app form {
  background-color: #a88e1b;
}
#app button {
  background-color: #7f03fc;
  border: 0px;
  border-radius: 5px;
  font-size: 1.25rem;
  color: white;
  font-family: 'Times New Roman', Times, serif;
  margin-top: 10px;
}
#app .data-container {
  list-style: none;
  background-color: #226600;
}
#app .data-container h2,
h3 {
  font-size: 1.25rem;
  color: #000b9e;
  font-family: 'Franklin Gothic Medium';
}
#app .data-container label {
  font-size: 1rem;
  font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
  width: 50px;
  display: inline-block;
  font-weight: bold;
  color: #5c116b;
  text-align: center !important;
  display: inline-block;
  width: 100%;
}
</style>
