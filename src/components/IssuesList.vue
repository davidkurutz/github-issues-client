<template>
  <div id="main">
    <h1>Git Issues Client</h1>
    <div class="row well">
      <div class="col-md-6">
        <h4>Title</h4>
      </div>
      <div class="col-md-2">
        <h4>Status</h4>
      </div>
      <div class="col-md-2">
        <h4>Created At</h4>
      </div>
      <div class="col-md-2">
        <h4>User</h4>
      </div>
    </div>
    <issue v-for="issue in issues" :issue="issue"></issue>
  </div>
</template>

<script type="text/javascript">

import Issue from './Issue';

export default {
  props: ['issues'],
  components: {
    Issue,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  #main {
    width: 1100px;
    padding-top: 20px;
    margin: 0 auto;
  }
</style>
