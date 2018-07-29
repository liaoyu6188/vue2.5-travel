<template>
  <div>
    <div class="banner" @click="handleBannnerClick">
    	<img class="banner-img" src="//img1.qunarzz.com/sight/p0/1411/d8/eec44461ecfd83df9c1669e7846b1c53.water.jpg_600x330_c147682d.jpg" />
    	<div class="banner-info">
    	  <div class="banner-title">蜈支洲岛(AAAAA景区)</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe692; </span>39
        </div>
    	</div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1411/6c/277a999f3b36d6a848c7e1f3108f2ea1.water.jpg_r_800x800_8d34dd11.jpg', 'http://img1.qunarzz.com/sight/p0/1411/6c/277a999f3b36d6a848c7e1f3108f2ea1.water.jpg_r_800x800_8d34dd11.jpg']
    }
  },
  methods: {
    handleBannnerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary,
  }
}
</script>

<style lang="stylus" scoped>
.banner
  position: relative
  overflow: hidden
  height: 0
  padding-bottom: 55%
  .banner-img
    width: 100%
  .banner-info
    display: flex
    position: absolute
    left: 0
    right: 0
    bottom: 0
    line-height: .6rem
    color: #fff
    background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, .8))
    .banner-title
      flex: 1
      font-size: .32rem
      padding: 0 .2rem
    .banner-number
      height: .32rem
      margin-top: .14rem
      padding: 0 .4rem
      line-height: .32em
      border-radius: .2rem
      background: rgba(0, 0, 0, .8)
      font-size: .24rem
      .banner-icon
        font-size: .24rem
</style>