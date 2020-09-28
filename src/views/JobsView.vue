<template>
  <div>
    <p v-for="item in this.$store.state.job" v-bind:key="item[0]">
      <a v-bind:href="item.url">{{ item.title }}</a>
      <small>{{ item.time_ago }} | {{ item.domain }}</small>
    </p>
  </div>
</template>

<script>
export default {
  created() {
    this.$store.dispatch('FETCH_JOB');
  },
};
</script>

<style></style>
