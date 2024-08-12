<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld :msg="apiUrl ? apiUrl : 'Hello World !!'"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
    return {
      apiUrl: process?.env?.VUE_APP_API_URL // Access the environment variable here
    };
  },
  mounted() {
    console.log("API URL:", this.apiUrl);
    // You can now use this.apiUrl in your component
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
