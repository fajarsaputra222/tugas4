<template>
  <div>
    <h1>Data task</h1>

    <form v-on:submit.prevent="addTask">
      <input type="text" v-model="newTask" placeholder="Tambahkan tugas...">
      <button type="submit">Tambah Tugas</button>
    </form>

    <ul>
      <li v-for="task in tasks" :key="task.id">{{ task.name }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newTask: '',
      tasks: []
    }
  },
  methods: {
    addTask() {
      if (this.newTask.trim() !== '') {
        this.tasks.push({
          id: Date.now(),
          name: this.newTask
        });
        this.newTask = '';
      }
    }
  }
}
</script>

<style scoped>
/* Gaya CSS khusus untuk komponen ini */
</style>
