<template>
  <Navbar />
  <router-view />
</template>

<script>
import Navbar from './components/Navbar.vue';

export default {
  components: { Navbar },
};
</script>

<style>
body {
  background: #f2f2f2;
}
#app {
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  max-width: 600px;
  margin: 0 auto;
  color: #555;
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>
