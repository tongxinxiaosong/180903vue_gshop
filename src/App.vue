<template>
    <div id="App">
        <router-view/>
        <FooterGuide v-show="$route.meta.showFooter"/>
    </div>
</template>

<script>
import { mapActions } from 'vuex'// 映射函数
import FooterGuide from './components/FooterGuide/FooterGuide.vue'

export default{
  components: {
    FooterGuide
  },

  mounted () {
    // this.$store.dispatch('getAddress')
    this.getAddress()
  },

  methods: {
    ...mapActions(['getAddress'])
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .app
    width 100%
    height 100%
    background #f5f5f5
</style>
