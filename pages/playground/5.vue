<template>
  <div>
    <div>
      <h1>Even Number</h1>
      <p v-for="n in evenNumbers">{{ n }}</p>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        numbers: [1, 2, 3, 4, 5, 6, 7, 8, 9]
      }
    },
    computed: {
      evenNumbers() {
        this.numbers.filter((number) => {
          return this.numbers % 2 === 0;
        })
      }
    }
  }
</script>

<style>

</style>
