<template>
  <Schedule />
</template>

<script>
import Schedule from "./components/Schedule/Schedule.vue";

export default {
  name: "App",
  components: {
    Schedule,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  justify-content: center;
}
p {
  margin: 0;
}
</style>
