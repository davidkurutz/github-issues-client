<template>
  <div id="app">
    <!-- <todo-list v-bind:todos="todos"></todo-list> -->
    <issues-list v-bind:issues="issues"></issues-list>
    
  </div>
</template>

<script>
import IssuesList from './components/IssuesList';

const axios = require('axios');

export default {
  name: 'app',
  components: {
    IssuesList,
  },
  data() {
    return {
      issues: [],
    };
  },
  created() {
    axios.get('https://api.github.com/repos/rails/rails/issues').then((response) => {
      this.issues = response.data;
    });
  },
};
</script>

<style>
</style>
