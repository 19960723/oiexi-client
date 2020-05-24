<template>
  <div class="newsContainer">
    <product-head-com :lxl-title-top="'NEWS'" :lxl-title-bottom="'全景咨询'"></product-head-com>
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
export default class NewsCom extends Vue {}
</script>

<style lang="scss" scoped>

</style>
