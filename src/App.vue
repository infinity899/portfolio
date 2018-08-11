<template>
  <div id="app">
    <router-view/>
    <vue-particles color="#008ae6"
                   :particlesNumber="120"
    ></vue-particles>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>

* {
  padding: 0;
  margin: 0;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: #2c3e50;
}
</style>
