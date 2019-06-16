<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id"><img class="swiper-img" :src="item.imgUrl"/></swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://images2.alphacoders.com/678/thumb-1920-678024.png'
      }, {
        id: '0002',
        imgUrl: 'https://images3.alphacoders.com/888/thumb-1920-888562.jpg'
      }, {
        id: '0003',
        imgUrl: 'https://images2.alphacoders.com/872/thumb-1920-872499.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background #ffffff !important
  .wrapper
    overflow hidden
    width 100%
    background #eee
    .swiper-img
      width 100%
</style>
