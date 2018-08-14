<template>
  <div id="app">
    <router-view/>
    <button class="goTop" ref="topButton" v-if="isVisible" @click="backToTop">
      <i class="material-icons icon-lg">
        keyboard_arrow_up
      </i>
    </button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      isVisible: false
    }
  },
  methods: {
    backToTop() {
      window.scrollTo(0, 0);
      console.log(this.$refs.topButton);
    },
    initToTopButton() {
      let backToTopButton = this.$refs.topButton;
      console.log(backToTopButton);
      if (window.scrollY > 100) {
        this.isVisible = true;
      } else {
        this.isVisible = false;
      }
    }
  },
  mounted() {
    window.addEventListener('scroll', this.initToTopButton);
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
  box-sizing: border-box;
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
}

.content {
  display: flex;
  height: 100%;

  @media only screen and (max-width: $bp-medium) {
    flex-direction: column;
  }
}
.icon-lg {
  font-size: 32px;
}

.goTop {
  border-radius: 5px;
  background-color: rgb(1,14,27);
  background-color: rgba(1, 14, 27, .7);
  position: fixed;
  width: 45px;
  height: 45px;
  display: block;
  right: 15px;
  bottom: 15px;
  border: none;
  opacity: .8;
  z-index: 4;
  .material-icons {
    color: white;
    font-size: 24px;
  }

  &:hover {
    opacity: 1;
    background-color: rgb(1,14,27);
    background-color: rgba(1, 14, 27, .9);
  }
}

.isVisible {

  transition: all .4s ease-in;
}

.sidebar {
  flex: 0 0 18%;
  font-size: 16px;
  background-color: #333;
  color: #FFFFFF;

  &-menu {
    list-style: none;

    @media only screen and (max-width: $bp-medium) {
      display: flex;
      align-items: center;
    }
  }
}

</style>
