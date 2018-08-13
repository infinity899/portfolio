<template>
  <div class="container">
    <div class="content">
      <navbar></navbar>
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

</style>
