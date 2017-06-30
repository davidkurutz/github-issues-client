<template>
  <div>
    <ul>
      <issue>
        <li v-for="issue in issues">{{ issue.title }}</li>
      </issue>
    </ul>
  </div>
</template>

<script>
export default {
  props: ['issues'],
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

</style>
