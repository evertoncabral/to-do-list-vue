<template>
  <div>
    <h1>to do list com vue</h1>
    <input v-model.trim="task" />
    <button type="button" @click="addTasks">Adicionar</button>
    {{ task }}
    <ul>
      <li v-for="obj in tasks" :key="obj">{{ obj }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "ToDoList",
  data() {
    return {
      task: "",
      tasks: [],
    };
  },
  methods: {
    addTasks() {
      this.tasks.push(this.task);
      this.task = "";
    },
  },
};
</script>

<style>
</style>