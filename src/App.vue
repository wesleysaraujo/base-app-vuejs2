<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <messages></messages>
  </div>
</template>

<script>
import Messages from './components/Messages';

export default {
  name: 'app',
  components: {
    Messages,
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
