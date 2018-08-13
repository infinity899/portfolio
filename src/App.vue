<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
    }
  }
}
</script>

<style lang="scss">
@import "/scss/variables";

:root {
  --color-primary: #2c3e50;
  --color-primary-light: #FF3366;
  --color-primary-dark: #BA265D;

  --color-grey-light-1: #faf9f9;
  --color-grey-light-2: #f4f2f2;
  --color-grey-light-3: #f0eeee;
  --color-grey-light-4: #ccc;

  --color-grey-dark-1: #333;
  --color-grey-dark-2: #777;
  --color-grey-dark-3: #999;

  --shadow-dark: 0 2rem 6rem rgba(0,0,0,.3);
  --shadow-light: 0 2rem 5rem rgba(0,0,0,.06);

  --line: 1px solid var(--color-grey-light-2);
}

* {
  padding: 0;
  margin: 0;
}

/*Fix IOS bounce bug*/
html,
body {
  background-color: #2c3e50;
  height: 100%;
  font-size: 62.5%
}

#app {
  font-family: sans-serif, Helvetica, Arial;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  height: 100%;
}

.container {
  max-width: 1000px;
  margin: 8rem auto;
  background-color: #faf9f9;
  box-shadow: 0 2rem 6rem rgba(0,0,0,.3);
  min-height: 50rem;
  height: 100%;
}

.content {
  display: flex;
  height: 100%;
}

.sidebar {
  flex: 0 0 18%;
  font-size: 16px;
  background-color: #333;
  color: #FFFFFF;

  &-menu {
    list-style: none;
  }
}

</style>
