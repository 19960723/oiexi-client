<template>
  <div class="productTitle">
    <h1>{{lxlTitleTop}}</h1>
    <span>{{lxlTitleBottom}}</span>
  </div>
</template>

<script>
export default {
  props: {
    lxlTitleTop: String,
    lxlTitleBottom: String
  }
}
</script>

<style lang="scss" scoped>
.productTitle{
  padding: 30px 0;
  text-align: center;
  h1{
    font-weight: bold;
    font-size: 27px;
    display: inline-block;
    position: relative;
    line-height: 40px;
    font-family: 'arial black';
    &::before{
      content: "";
      position: absolute;
      border-bottom: 3px solid #c74751;
      left: 40%;
      right: 40%;
      bottom: 0;
      transition: 0.5s all;

    }
  }
  span{
    font-family: '黑体';
    font-size: 18px;
    line-height: 30px;
    display: block;
  }
}
</style>
