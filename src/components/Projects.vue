<template>
  <div class="container">
    <div class="content">
      <navbar></navbar>
      <div class="container-projects">
        <div class="intro-container">
          <p class="project-info"><i class="material-icons">format_quote</i>If one does not know to which port one is sailing, no wind is favorable<i class="material-icons">format_quote</i> - Seneca</p>
        </div>
        <div class="project">
          <div class="project-image-wrapper">
            <div class="project-image">
              <img src="../assets/darts.png" alt="project">
            </div>
          </div>
          <div class="project-description">
            <h3 class="project-title">Darts Tracker</h3>
            <p class="project-info">I built a Darts Tracker for our favourite darts game 301 using Vuejs</p>
            <a class="project-link" target="_blank" href="https://infinity899.github.io/"> Visit project
              <i class="material-icons">
                keyboard_tab
              </i>
            </a>
          </div>
        </div>
        <div class="project">
          <div class="project-image-wrapper">
            <div class="project-image">
              <img src="../assets/helvetia.png" alt="project">
            </div>
          </div>
          <div class="project-description">
            <h3 class="project-title">Helvetia</h3>
            <p class="project-info">Together with my peers at Epoint we built an online shop for Helvetia, a shop for luxury watches. We used magento, SASS and jQuery</p>
            <a class="project-link" target="_blank" href="https://helvetia.com.ro/"> Visit project
              <i class="material-icons">
                keyboard_tab
              </i>
            </a>
          </div>
        </div>
        <div class="project">
          <div class="project-image-wrapper">
            <div class="project-image">
              <img src="../assets/bierguide.png" alt="project">
            </div>
          </div>
          <div class="project-description">
            <h3 class="project-title">Beer Guide</h3>
            <p class="project-info">At Epoint we also had to take care for the thirsty people, so we built for a client a CMS project to help users find the best beer experience using Drupal8, SASS and jQuery</p>
            <a class="project-link" target="_blank" href="http://bier-guide.net/"> Visit project
              <i class="material-icons">
                keyboard_tab
              </i>
            </a>
          </div>
        </div>
        <div class="project">
          <div class="project-image-wrapper">
            <div class="project-image">
              <img src="../assets/medianettv.png" alt="project">
            </div>
          </div>
          <div class="project-description">
            <h3 class="project-title">Medianet TV</h3>
            <p class="project-info">We built a video platform for our client using Drupal8, SASS and Vuejs</p>
            <a class="project-link" target="_blank" href="https://tv.medianet.at/"> Visit project
              <i class="material-icons">
                keyboard_tab
              </i>
            </a>
          </div>
        </div>
        <div class="outro-container">
          <p class="tech-info">I am experienced and love working with:</p>
          <div class="tech-icons">
            <img src="../assets/javascript.svg" alt="js">
            <img src="../assets/jquery.svg" alt="jq">
            <img src="../assets/css.svg" alt="css">
            <img src="../assets/sass.svg" alt="sass">
            <img src="../assets/Vue.svg" alt="vue">
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

  .container-projects {
    padding: $sp-size-l;
  }

  .project {
    display: flex;
    margin-bottom: $sp-size-l;

    @media only screen and (max-width: $bp-medium) {
      flex-direction: column;
      align-items: center;
    }

    &-title {
      color: var(--color-primary);
      font-size: $f-size-xl;
      font-weight: 700;
      margin: $sp-size-m 0;
    }

    &-info {
      color: var(--color-grey-dark-2);
      padding: $sp-size-l;
      font-size: $f-size-m;
    }

    &-link {
      color: var(--color-primary);
      font-size: $f-size-m;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      justify-content: center;

      .material-icons {
        margin-left: $sp-size-xs;
      }
    }
  }

  .project-info {
    margin-bottom: $sp-size-l;
  }

  .project-image {
    flex-basis: 300px;
    flex-grow: 0;
    flex-shrink: 0;
    display: flex;
    align-items: center;
    margin-right: $sp-size-l;

    &-wrapper {
      background-color: var(--color-grey-dark-1);
      display: flex;
      flex-basis: 300px;
      flex-grow: 0;
      flex-shrink: 0;
      height: 200px;
      box-shadow: 8px 8px 10px 0 rgba(44, 62, 80, 1), 2px 2px 4px 2px rgba(44, 62, 80, 1);
      margin-bottom: $sp-size-l;

      @media only screen and (max-width: $bp-medium) {
        flex-basis: auto;
        height: 200px;
        width: 300px;
      }
    }

    img {
      width: 100%;
      height: auto;
      margin: auto;
    }
  }

  .tech-icons {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;

    img {
      width: 75px;
      height: 75px;

      &:not(:last-of-type) {
        margin-right: $sp-size-s;
      }
    }
  }

  .tech-info {
    color: var(--color-grey-dark-2);
    font-size: $f-size-m;
  }
</style>
