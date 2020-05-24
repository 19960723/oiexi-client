<template>
  <div class="homeContainer">
    <header-com class="header" :lxl-height="90" :lxl-logo="imgLogo">
      <template v-slot:head>
        <ul class="headList">
          <li class="item" v-for="item in navList" :key="item.id" :class="{'active': curSort === item.id}" @click="navHandle(item.id)">{{item.name}}</li>
        </ul>
      </template>
    </header-com>
    <banner-swiper></banner-swiper>
    <home-com></home-com>
    <footer-com ref="footer"></footer-com>
  </div>
</template>

<script>
import headerCom from '@/components/header'
import bannerSwiper from '@/components/Home/bannerSwiper'
import homeCom from '@/components/Home'
import footerCom from '@/components/footer'
export default {
  name: 'homePage',
  data () {
    return {
      imgLogo: require('@/assets/images/oiexi_logo.png'),
      curSort: 1,
      navList: [
        { id: 1, name: '首页', active: 'true' },
        { id: 2, name: '关于我们' },
        { id: 3, name: '产品' },
        { id: 4, name: '资讯' },
        { id: 5, name: '合作伙伴' },
        { id: 6, name: '加入我们' }
      ]
    }
  },

  mounted () {
    console.log(this.$refs.footer.$el)
  },

  methods: {
    navHandle (id) {
      this.curSort = id
    }
  },

  components: {
    headerCom,
    bannerSwiper,
    footerCom,
    homeCom
  }
}
</script>

<style lang="scss" scoped>
.header{
  width: 100%;
  background: #821A1A;
  .headList{
    display: flex;
    justify-content: space-around;
    .item{
      width: 100%;
      text-align: center;
      color: #ccc;
      font-size: 12px;
      user-select: none;
      cursor: pointer;
      &.active{
        background: rgba(0, 0, 0, 0.1);
        color: #fff;
        font-size: 17px;
      }
    }
  }
}
</style>
