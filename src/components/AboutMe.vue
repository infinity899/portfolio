<template>
<div class="container">
  <div class="content">
    <navbar></navbar>
    <div class="container-text-box">
      <div class="text-box-wrapp">
        <p class="text-description m-btn">
          <i class="material-icons">format_quote</i>
          It always seems impossible until it's done
          <i class="material-icons">format_quote</i>
          - Nelson Mandela
        </p>
      </div>
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
        <p class="text-description">Graduated Politehnica Timisoara University with a degree in Computer Science</p>
      </div>
      <div class="text-box-wrapper">
        <i class="material-icons">casino</i>
        <h3 class="text-years">2012-2017</h3>
        <p class="text-description">Professionally played online poker, using my analytical thinking and interpreting hands and statistics saved in a database I had an edge against the players. Over these 5 years I had a 25% ROI</p>
      </div>
      <div class="text-box-wrapper">
        <i class="material-icons">web</i>
        <h3 class="text-years">2017-Present</h3>
        <p class="text-description">I retired from poker and started working in Timisoara as a frontend engineer at <a href="http://www.epoint.ro/" target="_blank" class="epoint-link">Epoint</a>, where we make the internet better and more beautiful using technologies like javascript, Vuejs, SASS, Drupal, Magento and jQuery</p>
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
}
.material-icons {
  color: var(--color-primary);
  font-size: $f-size-xl;
}

.text-box-wrapper {
  display: flex;
  flex-direction: column;

  &::after {
    background: var(--color-primary);
    content: '';
    display: block;
    height: 2px;
    margin: $sp-size-m auto;
    width: 60%;
  }
}

.epoint-link {
  color: var(--color-primary);
}

.m-btn {
  margin-bottom: $sp-size-l
}

</style>
