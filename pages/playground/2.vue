<template>
  <div>
    <div v-html="htmlRaw"></div>
    <v-btn color="blue" :disabled="isDisabled">Click Me</v-btn>
    <v-btn color="yellow" @click="changeStatus">Change Status</v-btn>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        htmlRaw: '<h2>Raw HTML</h2>',
        isDisabled: false
      }
    },
    methods: {
      changeStatus() {
        this.isDisabled = !this.isDisabled;
      }
    }
  }
</script>

<style>

</style>
