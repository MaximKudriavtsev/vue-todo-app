<template>
  <ul>
    <li v-for="(task, index) in tasks" :key="index">
      {{ task.index }} <span>{{ task.text }}</span> <span v-on:click="deleteTask(task.id)">[x]</span>
    </li>
    <hr />
    <Task
      v-for="(task, index) in tasks"
      :key="index"
      :index="task.id"
      :text="task.text"
      :deleteF="deleteTask"
    />
  </ul>
</template>

<script>
/* eslint-disable */
import Task from './Task'

export default {
  name: 'TaskList',
  components: {
    Task
  },
  data () {
    return ({
      tasks: [
        { id: 0, text: 'First task' },
        { id: 1, text: 'Second task' },
        { id: 2, text: 'Third task' },
        { id: 3, text: 'Thourth task' }
      ]
    });
  },
  methods: {
    deleteTask: function (id) {
      const nextTasks = this.tasks;
      const deletedIndex = nextTasks.findIndex(task => task.id === id);
      nextTasks.splice(deletedIndex, 1);

      this.tasks = nextTasks;
    }
  }
}
</script>
