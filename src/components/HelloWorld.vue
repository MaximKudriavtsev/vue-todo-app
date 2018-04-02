<template>
  <div class="hello">
    <ul>
      <li v-for="(user, index) in users" :key="index">
        {{ user.firstname }} {{ user.lastname }}
      </li>
    </ul>
    <input type="text" v-model="input_val">
    Input Values: <span v-text="input_val"></span>
    <hr />
    <div>
      <button class="btn btn-promary" v-on:click="counter++">
        You've clicked this button {{ counter }} times!
      </button>
    </div>
  </div>
</template>

<script>
/* eslint-disable */
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      users: [
        {firstname: 'Sebastian', lastname: 'Eschweiler'},
        {firstname: 'Bill', lastname: 'Smith'},
        {firstname: 'John', lastname: 'Porter'}
      ],
      input_val: '',
      counter: 0
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
