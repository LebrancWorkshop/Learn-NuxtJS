<template>
  <div>
    <div id="inputship">
      <h1>Input Message</h1>
      <v-text-field
        v-model="inputMessage"
        label="Input Message"
      ></v-text-field>
      <p>Input Message: {{ inputMessage }}</p>
    </div>
    <div id="task">
      <Task v-for="task in tasks" :key="task.id" :task="task" />
    </div>
  </div>
</template>

<script>
  import Task from '@/components/Task.vue';
  export default {
    data() {
      return {
        inputMessage: '',
        tasks: [
          { id: 1, title: 'Learn History' },
          { id: 2, title: 'Learn Math' },
          { id: 3, title: 'Learn Science' },
          { id: 4, title: 'Learn English' },
          { id: 5, title: 'Learn Geography' }
        ]
      }
    }
  }
</script>

<style>
  #inputship {
    width: 30%;
  }
</style>
