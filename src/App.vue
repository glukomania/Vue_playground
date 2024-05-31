<template>
  <input type="text" v-model="userName" placeholder="Name">
  <input type="email" v-model="userEmail" placeholder="Email">
  <input type="password" v-model="userPassword" placeholder="Password">
  <p>{{ userName }}</p>
  <p>{{ userEmail }}</p>
  <p>{{ userPassword }}</p>

</template>

<script>
  export default {
    data() {
      return {
        userName: '',
        userEmail: '',
        userPassword: ''
      }
    },
    methods: {
    }
  }
</script>

<style scoped>
h1 {
  color: red;
}
p {
  color: green;
}
</style>
