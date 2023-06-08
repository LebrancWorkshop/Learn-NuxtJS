<template>
  <div>
    <p>Original Message: {{ message }}</p>
    <p>Reverse Message: {{ reversedMessage }}</p>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        message: 'Hello World'
      }
    },
    computed: {
      reversedMessage() {
        return this.message.split('').reverse().join('');
      }
    }
  }
</script>

<style>

</style>
