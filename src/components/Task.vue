<template>
  <li>
    {{ index }} <span>{{ text }}</span><span v-on:click="deleteF(id)">[x]</span>
  </li>
</template>

<script>
/* eslint-disable */
export default {
  name: 'Task',
  props: {
    index: Number,
    text: String,
    deleteF: Function,
    id: Number,
  }
}
</script>
