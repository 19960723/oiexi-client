<template>
  <div id="app">
    <header-com class="header" :lxl-height="90" :lxl-logo="imgLogo">
      <template v-slot:head>
        <ul class="headList">
          <li class="item" v-for="item in showNavList()" :key="item.id" :class="{'active': curSort === item.id}" @click="navHandle(item)">{{item.name}}</li>
        </ul>
      </template>
    </header-com>
    <router-view/>
    <footer-com></footer-com>
  </div>
</template>

<script lang="ts">
import { Vue, Component, Watch } from 'vue-property-decorator'
import footerCom from '@/components/footer/index.vue'
import headerCom from '@/components/header/index.vue'
@Component({
  components: {
    footerCom,
    headerCom
  },
  mounted () {
    this.navList.forEach(item => {
      if (item.path === this.$route.path) {
        this.curSort = item.id
      }
    })
  }
})
export default class extends Vue {
  imgLogo = require('@/assets/images/oiexi_logo.png')
  curSort = 1
  navList = [
    { id: 1, name: '首页', active: 'true', path: '/' },
    { id: 2, name: '关于我们', path: '/about' },
    { id: 3, name: '产品', path: '/product' },
    { id: 4, name: '资讯', path: '/news' },
    { id: 5, name: '合作伙伴' },
    { id: 6, name: '加入我们' }
  ]
  // methods

  @Watch('$route')
  routerchange (to: any, from: any) {
    // this.navList.forEach(item => {
    //   if (item.path === to.path) {
    //     console.log(item)
    //   }
    // })
    this.showNavList()
  }

  navHandle (item) {
    this.curSort = item.id
    if (item.path) {
      this.routerHandle(item.path)
    }
  }

  routerHandle (path) {
    this.$router.push({
      path: path
    }).catch((err: any) => {
      return err
    })
  }

  // computed

  showNavList () {
    let list = []
    if (this.$route.path === '/') {
      list = this.navList
    } else {
      list = this.navList.filter((item) => {
        if (item.path) {
          return item
        }
      })
    }
    return list
  }
}

</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
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
