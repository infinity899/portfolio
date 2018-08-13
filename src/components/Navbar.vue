<template>
<nav class="sidebar">
  <ul class="sidebar-menu">
    <li class="side-nav__item">
      <router-link class="side-nav__link" to="/about">About Me</router-link>
    </li>
    <li class="side-nav__item">
      <router-link class="side-nav__link" to="/projects">Projects</router-link>
    </li>
    <li class="side-nav__item">
      <router-link class="side-nav__link" to="/contact">Contact</router-link>
    </li>
  </ul>
</nav>
</template>
<script>
  export default {
    data () {
      return {
      }
    }
  }
</script>
<style lang="scss" scoped>
  @import "../scss/variables";

  .router-link-active {
    background-color: var(--color-primary);
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

  .side-nav {
    font-size: 1.4rem;
    list-style: none;
    margin-top: 3.5rem;

    @media only screen and (max-width: $bp-medium) {
      display: flex;
      margin: 0;
    }

    &__item {
      position: relative;
      font-weight: 700;
      letter-spacing: 1px;
      width: 100%;
      margin-left: 0;
      margin-right: 0;

      &:not(:last-child) {
        margin-bottom: .5rem;

        @media only screen and (max-width: $bp-medium) {
          margin: 0;
        }
      }

      &:first-child {
        margin-top: 32px;
      }

      @media only screen and (max-width: $bp-medium) {
        flex: 1;
      }
    }

    &__item::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 3px;
      background-color: var(--color-primary);
      transform: scaleY(0);
      transition: transform .2s,
      width .4s cubic-bezier(1, 0, 0, 1) .2s,
      background-color .1s;
    }

    &__item:hover::before,
    .router-link-active::before {
      transform: scaleY(1);
      width: 100%;
    }

    .router-link-active::before {
      background-color: var(--color-primary);
    }

    &__link:link,
    &__link:visited {
      color: var(--color-grey-light-1);
      text-decoration: none;
      text-transform: uppercase;
      display: block;
      padding: 1.5rem 3rem;
      position: relative;
      z-index: 10;

      @media only screen and (max-width: $bp-medium) {
        justify-content: center;
        padding: 2rem;
      }

      @media only screen and (max-width: $bp-small) {
        flex-direction: column;
        padding: 1.5rem .5rem;
      }
    }
  }

</style>
