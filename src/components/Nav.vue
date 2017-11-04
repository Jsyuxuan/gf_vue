<template>
  <nav>
    <div class="nav_bar" @click="_nav_open"></div>
    <div class="nav_content">
      <ul>
        <li>111111111</li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods: {
    _nav_open () {
      this.$emit('nav_open')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
  nav
    position fixed
    left 0
    top 0
    width 100px
    height 100%
    z-index 800
    transform translate3d(0, 0, 0)
    .nav_bar
      position relative
      width 100px
      height 100%
      padding-top 2.125em
      background-color #212121
      z-index 9999
      cursor pointer
    .nav_content
      position absolute
      width 300px
      height 100%
      right 100px
      top 0
      background-color #060606
      transform translate3d(0, 0, 0)
      transition opacity 487ms ease-out 123ms
</style>
