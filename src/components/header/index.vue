<template>
  <div class="headerContainer" :style="{ height: lxlHeight + 'px', lineHeight: lxlHeight + 'px' }">
    <div class="lxl-header">
      <div class="nav-left">
        <img :src="lxlLogo" alt="">
      </div>
      <div class="nav-right">
        <slot name="head"></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'headerCom',
  props: { lxlHeight: Number, lxlLogo: String }
}
</script>

<style lang="scss" scoped>
.headerContainer{
  .lxl-header{
    height: 100%;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    .nav-left{
      height: 100%;
      width: 30%;
      img{
        width: 100%;
        height: 100%;
      }
    }
    .nav-right{
      width: 50%;
      height: 100%;
    }
  }
}
</style>
