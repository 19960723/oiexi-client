<template>
  <div>
    <product-Head-com :lxl-title-top="'PARTNER'" :lxl-title-bottom="'合作伙伴'"></product-Head-com>
    <div class="firend_logo_list">
      <li class="item" v-for="item in logoList" :key="item">
        <img :src="item" alt="">
      </li>
    </div>
  </div>
</template>

<script>
import productHeadCom from '../productHead'

export default {
  data () {
    return {
      logoList: [
        require('@/assets/images/friend_logo/华为.png'),
        require('@/assets/images/friend_logo/联想.png'),
        require('@/assets/images/friend_logo/oiexi_logo.png'),
        require('@/assets/images/friend_logo/AMD.png'),
        require('@/assets/images/friend_logo/奥图码.png'),
        require('@/assets/images/friend_logo/爱普生.png'),
        require('@/assets/images/friend_logo/理光.png'),
        require('@/assets/images/friend_logo/科视.png'),
        require('@/assets/images/friend_logo/英伟达.png'),
        require('@/assets/images/friend_logo/英特尔.png')
      ]
    }
  },

  components: {
    productHeadCom
  }
}
</script>

<style lang="scss" scoped>
.firend_logo_list{
  width: 70%;
  margin: 0 auto 40px;
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  background: rgba(0, 0, 0, 0.1);
  .item{
    flex: 20%;
    height: 100px;
    position: relative;
    img{
      width: 100%;
      height: 100%;
      transform: scale(0.8);
    }
  }
}
</style>
