<!--  -->
<template lang="html">
  <div :class="$style.header">
    <span :class="$style.left">
      <em>注册</em>&nbsp;|&nbsp;<em>登录</em>
    </span>
    <btn :class="$style.btnDownload">APP下载</btn>
  </div>

</template>

<script>
import btn from '../core/btn.vue'
export default {
  components: { btn }
}

</script>
<style lang='scss' module>
.header {
  color: #666;
  height: 100px;
  line-height: 100px;
  position: fixed;
  top: 0px;
  left: 0px;
  right: 0px;
  font-size: 32px;
  background: #fff url("../../images/jr-logo.png") center center no-repeat;
  background-size: auto 50%;
  z-index: 100px;
  .left {
    font-size: 28px;
    height: 30px;
    line-height: 30px;
    margin: 17px 0 0 18px;
  }
  .btnDownload {
    float: right;
    font-size: 24px !important;
    border-width: 0;
    height: 56px;
    line-height: 56px !important;
    min-width: 120px;
    border-radius: 4px;
    margin: 28px 24px 0 0;
  }
}
</style>
