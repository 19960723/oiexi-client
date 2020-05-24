<template>
  <div class="swiperContainer lxl-swiper">
    <swiper ref="mySwiper" :options="swiperOptions">
      <swiper-slide v-for="item in bannerImage" :key="item"><img :src="item" alt=""></swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'bannerSwiper',
  data () {
    return {
      swiperOptions: {
        pagination: {
          el: '.swiper-pagination'
        },
        autoplay: {
          delay: 3000,
          disableOnInteraction: false
        },
        loop: true
      },
      bannerImage: [
        'http://asd.oiexi.com/image/default/032321B9C01E4D4698B31BC9454084F1-6-2.jpg',
        'http://asd.oiexi.com/image/default/328AD04776BB42A2B9239E363EF9D3D4-6-2.jpg',
        'http://asd.oiexi.com/image/default/68106D3258F54345BD1E91DECF4BF44E-6-2.jpg',
        'http://asd.oiexi.com/image/default/A468828C0F98455C9E2C2E4C59EE6021-6-2.jpg'
      ]
    }
  },

  computed: {
    swiper () {
      return this.$refs.mySwiper.$swiper
    }
  }
}
</script>

<style lang="scss" scoped>
.swiperContainer{
  cursor: pointer;
}
.swiper-container{
  height: 100%;
  img{
    width: 100%;
    height: 100%;
  }
}
</style>
<style lang="scss">
.swiperContainer{
  .swiper-pagination-bullet-active{
    background: #fff;
    width: 10px;
    height: 10px;
  }
}

</style>
