<template>
  <div class="container">
    <div class="content">
      <navbar></navbar>
      <div class="container-contact">
        <div class="contact-text-box">
          <p class="contact-info">
            <i class="material-icons">format_quote</i>
            Inventors and geniuses have almost always been looked on as no better than fools at the beginning of their career, and very frequently at the end of it also.
            <i class="material-icons">format_quote</i>
            - Dostoievski
          </p>
          <p class="contact-info">I am very passionate about web development. A self-motivated person, preoccupied about personal development, tech, books and entrepreneurship </p>
          <p class="contact-info">If you have the next one billion-dollar idea, want to know me better or just want to chat with me you can find me on:</p>
          <div class="contact-icons">
            <a href="https://www.facebook.com/andrei.pirvulescu.14" target="_blank"><img src="../assets/facebook.svg" alt="facebook" class="svg-icon"></a>
            <a href="https://www.linkedin.com/in/andrei-eduard-pirvulescu-9a3795142/" target="_blank"> <img src="../assets/linkedin.svg" alt="linked" class="svg-icon"></a>
            <a href="https://www.instagram.com/infinity_3.14/" target="_blank"><img src="../assets/instagram.svg" alt="insta" class="svg-icon"></a>
            <a href="mailto:pirvulescu.andrei91@yahoo.com"><img src="../assets/mail.svg" alt="mail" class="svg-icon">
            </a>
          </div>
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

  .contact-info {
    color: var(--color-grey-dark-2);
    padding: $sp-size-xl;
    font-size: $f-size-m;
    line-height: 1.6;
    font-weight: 500;
  }

  .contact-icons {
    display: flex;
    align-items: center;
    justify-content: space-around;
  }

  .svg-icon {
    width: 50px;
    height: 50px;
  }

  .container {
    @media only screen and (min-width: $bp-medium + 1) {
      height: 100%;
    }
  }

</style>
