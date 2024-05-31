<template>
  <input type="text" @input="insertData($event.target.value)" placeholder="Name">
  <input type="email" placeholder="Name">
  <input type="password" placeholder="Name">
  <p>{{ userName }}</p>

</template>

<script>
  export default {
    data() {
      return {
        userName: '',
        email: '',
        password: ''
      }
    },
    methods: {
      insertData(val) {
        this.userName = val
      }
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
