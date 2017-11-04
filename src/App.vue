<template>
  <div id="app" :class="{'nav_open': navOpen}">
    <G-nav @nav_open="open"></G-nav>
    <main></main>
  </div>
</template>

<script>
  import GNav from './components/Nav'
  export default {
    name: 'app',
    data () {
      return {
        navOpen: false
      }
    },
    components: {
      GNav
    },
    methods: {
      open () {
        this.navOpen = true
      }
    }
  }
</script>

<style lang="stylus">
  *, *:before, *:after
    -moz-box-sizing border-box
    -webkit-box-sizing border-box
    box-sizing border-box
  html,body,#app
    height 100%
  body
    margin 0
    background-color #060606
  #app
    transform: translate3d(0, 0, 0);
    transition: transform 287ms cubic-bezier(0.215, 0.61, 0.355, 1);
  .nav_open
    transform translateX(300px)!important
  main
    position relative
    height 100%
    padding-left 100px
    overflow hidden
    z-index 6
</style>
