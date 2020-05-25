<template>
  <div class="caseShowContainer">
    <div class="case_slide">
      <h1>全景案例展示</h1>
      <div class="case_slide_list">
        <swiper ref="mySwiper" :options="swiperOptions">
          <swiper-slide v-for="(item, index) in sceneShow" :key="index">
            <img :src="item" alt="">
          </swiper-slide>
        </swiper>
        <div class="swiper-button-next" :style="{ backgroundImage: 'url('+ nextIcon +')'}"></div>
        <div class="swiper-button-prev" :style="{ backgroundImage: 'url('+ preIcon +')'}"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'caseShowCam',
  data () {
    return {
      swiperOptions: {
        slidesPerView: 3,
        slidesPerColumn: 2,
        spaceBetween: 30,
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
        }
      },
      preIcon: require('@/assets/images/commont/pre_btn.png'),
      nextIcon: require('@/assets/images/commont/next_btn.png'),
      sceneShow: [
        'http://asd.oiexi.com/image/default/0E64BE1D87DE48CFA25CC031065271BB-6-2.jpg',
        'http://asd.oiexi.com/image/default/D65CE1369B8B4759A318160DA4724113-6-2.jpg',
        'http://asd.oiexi.com/image/default/CA65A7EBC4A446E49789B0BC173A5454-6-2.jpg',
        'http://asd.oiexi.com/image/default/BF7443B16FE24AF5A03402A6395B4CED-6-2.jpg',
        'http://asd.oiexi.com/image/default/715BC55DC0AA43D2973B6F9683E09757-6-2.jpg',
        'http://asd.oiexi.com/image/default/8D2B01142CBB409A8C0FEEA921B89E35-6-2.jpg',
        'http://asd.oiexi.com/image/default/E2309A5E90EB45A895CB72A264007128-6-2.jpg',
        'http://asd.oiexi.com/image/default/08F4D9FF66054AA295861C76590381B5-6-2.jpg',
        'http://asd.oiexi.com/image/default/08F4D9FF66054AA295861C76590381B5-6-2.jpg',
        'http://asd.oiexi.com/image/default/D135D0118477495EBD4CEB57ADE88A67-6-2.jpg'
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
.caseShowContainer{
  width: 100%;
  height: 500px;
  background: #000;
  .case_slide{
    width: 100%;
    height: 100%;
    background-image: url('http://asd.oiexi.com/image/default/B49675FD9F034260AE6B7AB6B09086E2-6-2.png');
    background-repeat: no-repeat;
    background-size: 100% 100%;
    background-position: 0 0;
    h1{
      text-align: center;
      font-size: 25px;
      font-weight: bold;
      color: #fff;
      font-family: "黑体";
      line-height: 100px;
    }
  }
  .case_slide_list{
    height: 330px;
    margin: 0 auto;
    position: relative;
    .swiper-container{
      height: 100%;
      width: 88%;
      .swiper-wrapper{
        flex-wrap: wrap;
        .swiper-slide{
          height: 150px;
          img{
            width: 100%;
            height: 100%;
          }
        }
      }
    }
    .swiper-button-prev{
      width: 40px;
      height: 40px;
      background-size: 100% 100%;
      &::after{
        content: '';
      }
    }
    .swiper-button-next{
      width: 40px;
      height: 40px;
      background-size: 100% 100%;
      &::after{
        content: '';
      }
    }
  }
}
</style>
