<template>
  <div class="footerContainer">
    <div class="lxl-footer">
      <div class="nav-footer">
        <div class="footer-info">
          <h3>联系我们</h3>
          <p>福州市鼓楼区工业路611号火炬高新技术创业园1号北楼506</p>
          <p>电话：4008-317-319</p>
          <p>邮箱：1363169592@qq.com</p>
        </div>
        <div class="footer-qrcode">
          <img :src="qrcode" alt="">
          <p>官方公众号</p>
        </div>
      </div>
      <div class="footer-ba">
        <span style="padding-right: 100px;">福州讯丰信息技术有限公司</span>
        <span>备案号：18018765号-1</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      qrcode: 'http://asd.oiexi.com/image/default/451A826EB17C4E709BA83A952C9B82F5-6-2.jpg'
    }
  }
}
</script>

<style lang="scss" scoped>
.footerContainer{
  width: 100%;
  background: #211717;
  font-family: '黑体';
  .lxl-footer{
    margin: 0 auto;
    color: #fff;
    .nav-footer{
      width: 100%;
      display: flex;
      justify-content: center;
      font-size: 15px;
      padding: 40px 0;
      p{
        padding-bottom: 8px;
      }
      .footer-info {
        h3{
          color: #31a0e1;
          font-size: 18px;
        }
      }
      .footer-qrcode{
        margin-left: 50px;
        img{
          width: 150px;
          height: 150px;
        }
        p{
          padding-top: 10px;
          text-align: center;
        }
      }
    }
    .footer-ba{
      display: flex;
      justify-content: center;
      border-top: 1px solid #201b25;
      line-height: 40px;
      color: rgb(178, 177, 177);
      font-size: 12px;
      text-align: center;
    }
  }
}
</style>
