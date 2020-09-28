<template>
  <div>
    <p v-for="item in this.$store.state.ask" v-bind:key="item[0]">
      <a v-bind:href="item.url"> {{ item.title }}</a>
      <small>{{ item.time_ago }} | {{ item.user }}</small>
    </p>
  </div>
</template>

<script>
import { mapGetters } from 'vuex';
export default {
  computed: {
    ...mapGetters(['fetchedAsk']),
  },
  created() {
    this.$store.dispatch('FETCH_ASK');
  },
};
</script>

<style></style>
