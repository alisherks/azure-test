<template>
  <div id="app">
    <p>ENV:</p>
    <ul>
      <li v-for="(value, key) in env" :key="key">
        <span style="font-weight: bold">{{key}}:</span> {{value}}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      env: {
        VUE_APP_TITLE: process.env.VUE_APP_TITLE,
        VUE_APP_SECRET: process.env.VUE_APP_SECRET,
        VUE_APP_MY_API_KEY: process.env.VUE_APP_MY_API_KEY,
      }
    };
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
ul {
  list-style: none;
  padding: 0;
  margin: 0;
}
li {
  margin: 0;
  padding: 0;
}
</style>
