<template>
  <div class="home">
    <vue-particles color="#008ae6"
                   :particlesNumber="120"
    ></vue-particles>
    <div class="home-container">
      <div class="avatar">
        <img src="../assets/avatar.png" alt="avatar" class="avatar-image">
      </div>
      <div class="avatar-about">
        <h2 class="avatar-name">Pirvulescu Andrei</h2>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">


.home-container {
  align-items: center;
  display: flex;
  flex-direction: column;
  position: absolute;
  transform: translate(-50%, -50%);
  left: 50%;
  top: 50%;
  z-index: 9999;
}

.avatar {
  border-radius: 50%;
  margin-bottom: 12px;
  overflow: hidden;
  width: 200px;

  &-image {
    height: auto;
    width: 100%;
  }

  &-about {
  }

  &-name {
    color: #FFFFFF;
    font-size: 32px;
    font-weight: 700;
    letter-spacing: 2px;

    &::after {
      background: #FFFFFF;
      content: '';
      display: block;
      height: 2px;
      margin: auto;
      width: 60%;
    }
  }
}

.home {
  overflow: hidden;
  position: relative;
}

#particles-js {
  height: 100vh;
}

h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
