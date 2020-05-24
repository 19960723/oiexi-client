<template>
  <div class="homeContainer">
    <about-com></about-com>
    <new-com ></new-com>
  </div>
</template>

<script>
import aboutCom from './about'
import newCom from './news'
export default {
  data () {
    return {
    }
  },

  components: {
    aboutCom,
    newCom
  }
}
</script>

<style lang="scss" scoped>
.homeContainer{
  background: url(http://asd.oiexi.com/image/default/0DE40720BD1444FD979A04563C27D256-6-2.jpg) 0px 0px / 100% 100% no-repeat;
  width: 100%;
  height: 100%;
}
</style>
<style>
.homeContainer{
  color: #000;
}
</style>
