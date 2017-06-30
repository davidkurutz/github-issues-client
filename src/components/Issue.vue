<template>
  <div class="row well">
    <div class="col-md-6">
      <a v-bind:href="issue.html_url">{{ issue.title }}</a>
    </div>
    <div class="col-md-2">
      {{ issue.state }}
    </div>
    <div class="col-md-2">
      {{ issue.created_at }}
    </div>
    <div class="col-md-2">
      <a v-bind:href="issue.user.html_url">{{ issue.user.login }}</a>
    </div>
  </div>
</template>

<script type="text/javascript">
  export default {
    props: ['issue'],
  };
</script>
