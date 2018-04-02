<template>
  <div id="app">
    <img src="./assets/logo.png">
    <HelloWorld/>
    <TaskList />
  </div>
</template>

<script>
/* eslint-disable */
import HelloWorld from './components/HelloWorld';
import TaskList from './components/TaskList';

export default {
  name: 'App',
  components: {
    HelloWorld,
    TaskList
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
