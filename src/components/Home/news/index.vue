<template>
  <div class="newsContainer">
    <product-head-com :lxl-title-top="'NEWS'" :lxl-title-bottom="'全景咨询'"></product-head-com>
    <div class="news_nav">
      <div class="news_show_left">
        <img src="http://asd.oiexi.com/image/default/9F462B8A899146D2B75A7AA501DC088C-6-2.jpg" alt="">
      </div>
      <div class="news_show_right">
        <div class="news_list_btn">
          <button>行业资讯</button>
          <button>媒体报道</button>
          <button>商业合作</button>
        </div>
        <div class="news_list_info">
          <li class="item" v-for="item in newsInfoList" :key="item.id">
            <img :src="item.imgSrc" alt="">
            <div class="news_info_message">
              <h3>{{item.title}}</h3>
              <p v-html="item.message"></p>
            </div>
            <span>{{item.curDate}}</span>
          </li>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import productHeadCom from '../productHead'
import { Vue, Component, Prop } from 'vue-property-decorator'
@Component({
  name: 'newsCom',
  components: {
    productHeadCom
  }
})
export default class NewsCom extends Vue {
  newsInfoList = [
    { id: 1, imgSrc: 'http://asd.oiexi.com/image/default/9F462B8A899146D2B75A7AA501DC088C-6-2.jpg', title: '全景巨幕入驻鲅鱼圈鼎红国际', message: '更狂欢、更酷炫尽在这里！', curDate: '2019-06-20' },
    { id: 2, imgSrc: 'http://asd.oiexi.com/image/default/020A225DFB4F43559075C496F97F7524-6-2.jpg', title: '福州讯丰携手雍和会给大家献上视觉盛宴', message: '这个六月福州讯丰携手雍和会给大家献上视觉盛宴', curDate: '2019-06-20' },
    { id: 3, imgSrc: 'http://asd.oiexi.com/image/default/D206C66245C6407098678A1FDAF91A04-6-2.jpg', title: '技术前沿丨你还在头疼你家KTV走廊单调吗？', message: '互动投影简介感应式互动投影系统主要针对新型多媒体内容而设计。<br> 本系统采用先进的计算机视觉技术和投影显示', curDate: '2019.03.31' }

  ]
}
</script>

<style lang="scss" scoped>
.newsContainer{
  .news_nav{
    height: 300px;
    margin: 0 auto;
    display: flex;
    .news_show_left{
      margin-right: 30px;
      height: 100%;
      img{
        width: 100%;
        height: 100%;
      }
    }
    .news_show_right{
      flex: 1;
      height: 100%;
      .news_list_btn{
        button{
          border: none;
          background: #c74751;
          color: #f2dbdc;
          padding: 5px 10px;
          margin-right: 4px;
        }
      }
      .news_list_info{
        width: 100%;
        height: 90%;
        display: flex;
        flex-wrap: wrap;
        .item{
          flex: 100%;
          display: flex;
          justify-content: space-between;
          align-self: flex-end;
          img{
            width: 140px;
            height: 80px;
          }
          .news_info_message{
            flex: 1;
            padding-left: 20px;
            padding-top: 10px;
            h3{
              font-family: "Adobe 黑体 Std";
              font-size: 16px;
              font-weight: normal;
            }
            p{
              color: #9e9c9c;
              line-height: 24px;
              font: 12px/1.5 "微软雅黑",Arial,Helvetica,sans-serif;
            }
          }
          span{
            font-size: 14px;
            color: #8d8d8d;
            padding-top: 40px;
          }
        }
      }
    }
  }
}
</style>
