<template>
  <input type="text" v-model="userName" placeholder="Name">
  <input type="email" v-model="userEmail" placeholder="Email">
  <input type="password" v-model="userPassword" placeholder="Password">
  <p className="error">{{ error }}</p>
  <button @click="sendData()">Send</button>

  <p>{{ users }}</p>

</template>

<script>
  export default {
    data() {
      return {
        users: [],
        userName: '',
        userEmail: '',
        userPassword: '',
        error: ''
      }
    },
    methods: {
      sendData() {
        console.log('Send is pressed')

        if(this.userName.length === 0){
          console.log('no name')
          this.error = 'No name entered'
          return
        }

        if(this.userEmail.length === 0){
          this.error = 'No email entered'
          return
        }

        if(this.userPassword.length === 0){
          this.error = 'No password entered'
          return
        }

        this.error = ''
        this.users.push({
          name: this.userName,
          email: this.userEmail,
          password: this.userPassword,
        })
      }
    }
  }
</script>

<style scoped>
  input {
    display: block;
    margin-bottom: 10px;
    border-radius: 3px;
    border: 1px solid silver;
    outline: none;
    padding: 10px 15px;
    background: #fafafa;
    color: #333
  }

  button {
    border: 0;
    padding: 10px;
    width: 100px;
    border-radius: 5px;
    background: #6cd670;
    color: #167f3d;
    font-weight: bold;
    cursor: pointer;
    transition: transform 500ms ease;
  }

  .user {
    width: 500px;
    margin-top: 20px;
    border: 1px solid silver;
    background: #e3e3e3;
    color: #222;
    padding: 20px;
    border-radius: 5px;
  }

</style>
