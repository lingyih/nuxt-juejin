<template>
  <div class="m-header">
    <div class="top">
      <div class="left">
        <lun-bannar :list="list"></lun-bannar>
      </div>
      <div class="right">
        假装这是个日历(｀・ω・´)
      </div>
    </div>
    <div class="content">
      <event-list v-for="(item, index) in cList" :key="index"></event-list>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
import lunBannar from '~/components/lunBannar/lunBannar.vue'
import eventList from '~/components/event/event.vue'
export default {
  data () {
    return {
      list: [
        {img: 'https://user-gold-cdn.xitu.io/153197025999312907462f883c163e56c6fbf2c9126bf.jpg?imageView2/1/w/460/h/270/q/85/format/webp/interlace/1'},
        {img: 'https://user-gold-cdn.xitu.io/153197025999312907462f883c163e56c6fbf2c9126bf.jpg?imageView2/1/w/460/h/270/q/85/format/webp/interlace/1'},
        {img: 'https://user-gold-cdn.xitu.io/153197025999312907462f883c163e56c6fbf2c9126bf.jpg?imageView2/1/w/460/h/270/q/85/format/webp/interlace/1'}
      ],
      cList: [
        {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}
      ]
    }
  },
  components: {
    lunBannar,
    eventList
  }
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
@import "~assets/css/base.styl";
.m-header
  height 900px
  width 960px
  margin  0 auto
  margin-top 20px
  text-align center
  .top
    width 100%
    height 280px
    display flex
    justify-content space-between
    .left
      width 470px
      height 100%
    .right
      width 470px
      height 100%
      background-color $color
      line-height 280px
      color $hcolor
      border-radius 3px
  .content
    display flex
    flex-wrap wrap
    margin-left 6px
</style>
