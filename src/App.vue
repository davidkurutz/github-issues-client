<template>
  <div id="app">
    <img src="./assets/logo.png">
    <hello></hello>
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
  data: {
    issues: [],
  },
  mounted() {
    axios.get('https://api.github.com/repos/rails/rails/issues').then((response) => { this.issues = response.data; });
    console.log(this.issues);
  },
};
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
