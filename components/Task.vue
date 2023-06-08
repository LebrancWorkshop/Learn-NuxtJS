<template>
  <div>
    <h1>{{ task.title }}</h1>
  </div>
</template>

<script>
  export default {
    props: ['task'],
    mounted() {
      console.table(this.task);
    }
  }
</script>

<style scoped>

</style>
