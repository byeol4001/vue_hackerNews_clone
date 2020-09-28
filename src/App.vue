<template>
  <div id="app">
    <tool-bar />
    <router-view></router-view>
  </div>
</template>

<script>
import ToolBar from './components/ToolBar.vue';
export default {
  methods: {
    fetchData() {
      console.log('aa');
    },
  },
  components: {
    ToolBar,
  },
};
</script>

<style>
#app {
  margin: 0;
  padding: 0;
}
</style>
