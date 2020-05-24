<template>
  <div class="aboutContainer">
    <product-head-com :lxl-title-top="'ABOUT US'" :lxl-title-bottom="'关于我们'"></product-head-com>
    <nav class="about_nav">
      <li class="item" v-for="item in aboutNavList" :key="item.id">
        <span>{{item.title}}</span>
        <i :style="{backgroundImage: 'url('+ item.icon +')'}"></i>
      </li>
    </nav>
    <section class="about_project">
      <div class="about_title_left">
        <h1>PROJECT</h1>
        <p>全景项目</p>
      </div>
      <nav class="image_nav_right">
        <li class="item" v-for="item in aboutProductList" :key="item.id">
          <div class="show_image">
            <div class="hover_project"></div>
            <img :src="item.showImage" alt="">
          </div>
          <p>{{item.info}}</p>
        </li>
      </nav>
    </section>
  </div>
</template>

<script>
import productHeadCom from '../productHead'
export default {
  name: 'aboutCom',
  data () {
    return {
      aboutNavList: [
        { id: 1, title: '全景项目', icon: require('@/assets/images/aboutNav/project_xm.png') },
        { id: 2, title: '全景咨询', icon: require('@/assets/images/aboutNav/project_zx.png') },
        { id: 3, title: '合作伙伴', icon: require('@/assets/images/aboutNav/project_hz.png') },
        { id: 4, title: '联系我们', icon: require('@/assets/images/aboutNav/project_lx.png') }
      ],
      aboutProductList: [
        { id: 1, showImage: 'http://asd.oiexi.com/image/default/4B38031DDCA040F0A52D9F537DD34233-6-2.png', info: '全景KTV' },
        { id: 2, showImage: 'http://asd.oiexi.com/image/default/DC750F4C80D64EFD817312618E6019DB-6-2.png', info: '全景餐厅' },
        { id: 3, showImage: 'http://asd.oiexi.com/image/default/F170E0451FC84F368F8B9B28F9399C40-6-2.png', info: '全景宴会厅' },
        { id: 4, showImage: 'http://asd.oiexi.com/image/default/314DA78330994D808B06AC6FE49925A1-6-2.png', info: '动感单车' },
        { id: 5, showImage: 'http://asd.oiexi.com/image/default/0B697EFCF92E4C4B8DB713A6F4922169-6-2.png', info: '全景茶室' }
      ]
    }
  },

  components: {
    productHeadCom
  }
}
</script>

<style lang="scss" scoped>
.aboutContainer{
  .about_nav{
    width: 70%;
    margin: 0 auto;
    display: flex;
    justify-content: space-around;
    line-height: 30px;
    i{
      display: block;
      width: 60px;
      height: 60px;
      margin: 20px auto;
      background-repeat: no-repeat;
      background-size: 100% 100%;
      background-position: 0 0;
    }
  }
  .about_project{
    width: 100%;
    background: url('http://asd.oiexi.com/image/default/248D2FD163944578A754FDEF397038F2-6-2.png') 0 0 no-repeat;
    background-size: 100% 100%;
    box-sizing: border-box;
    margin-top: 100px;
    display: flex;
    .about_title_left{
      float: left;
      color: #fff;
      width: 200px;
      padding-top: 20px;
      h1{
        font-weight: bold;
        font-size: 30px;
        font-family: 'arial black';
        display: inline-block;
        letter-spacing: 5px;
        line-height: 50px;
      }
      p{
        font-size: 18px;
        font-family: '黑体';
      }
    }
    .image_nav_right{
      float: right;
      flex: 1;
      display: flex;
      justify-content: space-around;
      .item{
        width: 100%;
        height: 100%;
        text-align: center;
        padding-right: 3%;
        box-sizing: border-box;
        transform: translateY(-50px);
        &:last-child{
          padding-right: 0;
        }
        .show_image{
          width: 100%;
          height: 90%;
          overflow: hidden;
          position: relative;
          .hover_project{
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.6);
            position: absolute;
            opacity: 0;
            left: 0;
            top: 0;
            z-index: 100;
            transform: translateY(-80%);
            transition: all .5s;
          }
          img{
            width: 100%;
            height: 100%;
            transition: all .5s;
          }
        }
        p{
          line-height: 50px;
          position: relative;
          top: 20px;
          color: #fff;
          text-align: right;
          letter-spacing: 3px;
          font-size: 18px;
          font-family: '黑体';
          &::before{
            content: '';
            position: absolute;
            right: 0;
            top: 0;
            width: 100%;
            height: 3px;
            background: #fff;
            transition: width .7s;
          }
        }
        &:hover{
          .show_image{
            .hover_project{
              transform: translateY(0);
              opacity: 1;
            }
          }
          cursor: pointer;
          p{
            &::before{
              width: 0;
            }
          }
        }
      }
    }
  }
}
</style>
