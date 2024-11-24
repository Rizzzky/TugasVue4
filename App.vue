// App.vue
<template>
  <div id="app">
    <h1>Sistem Komentar Nitizen</h1>
    <CommentList />
  </div>
</template>

<script>
import CommentList from './components/CommentList.vue';

export default {
  name: 'App',
  components: {
    CommentList,
  },
};
</script>

<style>
#app {
  font-family: Arial, sans-serif;
  padding: 20px;
  max-width: 1000px;
  margin: auto;
}
</style>
