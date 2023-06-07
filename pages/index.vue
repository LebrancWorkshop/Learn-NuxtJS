<template>
  <div>
    <header>
      <div v-bind:title="holdingMessage">
        <h1>Learn NuxtJS</h1>
        <h2>Learning for {{ learningTopic }}</h2>
      </div>
    </header>
    <section id="message-section">
      <div>
        {{ message }}
      </div>
    </section>
    <section id="action-section">
      <div>
        <v-btn color="primary" @click="reverse">
          Reverse
        </v-btn>
        <v-btn color="green" v-on:click="submit">
          Click to it
        </v-btn>
      </div>
    </section>
    <section id="list-section">
      <div v-for="(task, i) in tasks" :key="i">
        <v-checkbox
          v-model="task.completed"
          :label="task.name"
          :value="task.name"
        ></v-checkbox>
      </div>
    </section>
    <section id="input-section">
      <div>
        <v-text-field
          v-model="inputMessage"
          label="Input Message"
        ></v-text-field>
        <p>Input Message: {{ inputMessage }}</p> 
      </div>
    </section>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        learningTopic: 'Hello World',
        holdingMessage: 'Gravure',
        message: 'Hello World',
        canSee: false,
        tasks: [
          { name: 'Learn Nuxt', completed: false },
          { name: 'Learn Vue', completed: false },
          { name: 'Learn Laravel', completed: false },
          { name: 'Learn PHP', completed: false}
        ],
        inputMessage: ''
      }
    },
    methods: {
      submit() {
        console.log("AHA");
      },
      reverse() {
        this.message = this.message.split('').reverse().join('');
      }
    }
  }
</script>

<style>
  header {
    text-align: center;
  }

</style>
