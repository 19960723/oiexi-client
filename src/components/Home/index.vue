<template>
  <div class="homeContainer">
    <about-com></about-com>
    <new-com ></new-com>
    <partner-com></partner-com>
    <case-show-com></case-show-com>
  </div>
</template>

<script>
import aboutCom from './about'
import newCom from './news'
import partnerCom from './partner'
import caseShowCom from './caseShow'
export default {
  data () {
    return {
    }
  },

  components: {
    aboutCom,
    newCom,
    partnerCom,
    caseShowCom
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
