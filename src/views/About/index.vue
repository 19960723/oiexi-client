<template>
  <div class="aboutPageCntainer">
    <div class="about_show">
      <h1 class="title">企业背景</h1>
      <h3 class="message">COMPANY DESCRIPTION</h3>
      <p>福州讯丰信息技术有限公司是专业提供数字视觉技术及文化传媒服务的创意型科技企业。</p>
      <p>涉及的技术领域涵盖大屏拼接融合、水幕显示、3DMapping秀、LED冰屏、3D动漫制作、影像数据制作等可向各行业提供全景全息数字显示技术解决方案。</p>
      <p>公司致力以内容制作及软件定制为核心，以创意新颖的信息设计理念为导向，提供领先于国内多媒体行业的全方位数字视觉服务 </p>
      <p>公司以卓越的数字视觉技术服务于政府机构、夜景亮化、博览会、企业展厅、展馆、KTV娱乐场所等</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'aboutPage'
}
</script>

<style lang="scss" scoped>
.aboutPageCntainer{
  height: 500px;
  width: 100%;
  background: url('http://asd.oiexi.com/image/default/0DE40720BD1444FD979A04563C27D256-6-2.jpg') 0 0 no-repeat;
  background-size: 100% 100%;
  padding: 20px 0 50px;
  color: #000;
  .about_show{
    height: 100%;
    margin: 0 auto;
    padding: 60px 100px;
    box-sizing: border-box;
    .title{
      text-align: center;
      font-size: 30px;
      font-weight: normal;
    }
    .message{
      text-align: center;
      font-size: 20px;
      margin: 20px auto 20px;
      font-weight: normal;
    }
    p{
      font-size: 18px;
      text-align: left;
      line-height: 35px;
      font-family: "微软雅黑";
      text-indent: 2em;
    }
  }
}
</style>
