<template>
  <div class="homeContainer">
    <banner-swiper></banner-swiper>
    <home-com></home-com>
  </div>
</template>

<script>
import bannerSwiper from '@/components/Home/bannerSwiper'
import homeCom from '@/components/Home'
export default {
  name: 'homePage',
  components: {
    bannerSwiper,
    homeCom
  }
}
</script>

<style lang="scss" scoped>

</style>
