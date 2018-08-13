<template>
<div class="container">
  <div class="content">
    <navbar></navbar>
    <div class="container-text-box">
      <div class="text-box-wrapper">
        <i class="material-icons">child_care</i>
        <h3 class="text-years">1991</h3>
        <p class="text-description">I was born in Romania, Targu Jiu city</p>
      </div>
      <div class="text-box-wrapper">
        <i class="material-icons">school</i>
        <h3 class="text-years">2006-2010</h3>
        <p class="text-description">I went to Ecaterina Teodoroiu highschool to study mathematics and informatics</p>
      </div>
      <div class="text-box-wrapper">
        <i class="material-icons">school</i>
        <h3 class="text-years">2010-2014</h3>
        <p class="text-description">Graduated University Politehnica Timisoara with a degree in Computer Science</p>
      </div>
      <div class="text-box-wrapper">
        <i class="material-icons">casino</i>
        <h3 class="text-years">2012-2017</h3>
        <p class="text-description">Profesionaly played online poker</p>
      </div>
      <div class="text-box-wrapper">
        <i class="material-icons">web</i>
        <h3 class="text-years">2017-Present</h3>
        <p class="text-description">Working in Timisoara as a frontend engineer at Epoint</p>
      </div>
    </div>
  </div>
</div>
</template>
<script>
  import Navbar from '../components/Navbar.vue'
  export default {
    name: 'AboutMe',
    data () {
      return {
      }
    },
    components: {
      Navbar
    }
  }
</script>
<style lang="scss" scoped>
@import "../scss/variables";

.container-text-box {
  color: var(--color-grey-dark-2);
  padding: $sp-size-xl;
  width: 100%;
}

.text-years {
  color: var(--color-primary);
  font-size: $f-size-xl;
  font-weight: 700;
  margin: $sp-size-m 0;
}

.text-description{
  font-size: $f-size-m;

  &::after {
    background: var(--color-primary);
    content: '';
    display: block;
    height: 2px;
    margin: $sp-size-s auto;
    width: 60%;
  }
}
.material-icons {
  color: var(--color-primary);
  font-size: $f-size-xl;
}

.text-box-wrapper {
  display: flex;
  flex-direction: column;

  &:not(:last-of-type) {
    margin-bottom: $sp-size-m;
  }
}
</style>
