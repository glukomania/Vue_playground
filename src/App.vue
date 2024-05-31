<template>
  <h1>
    {{info}}
  </h1>
  <p>Some text</p>

  <button type="button" @click="this.info = 'Clicked'">Send</button>
</template>

<script>
  export default {
    data() {
      return {
        info: 'Title'
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
