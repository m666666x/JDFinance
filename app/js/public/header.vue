<!--  -->
<template lang="html">
    <div :class="$style.header">
        <span :class="$style.left">
            <em>注册</em>&nbsp;|&nbsp;<em>登录</em>
        </span><btn :class="$style.btnDownload">
            APP下载
        </btn>
    </div>
</template>

<script>
import bth from "../core/btn.vue"
export default {
    components: { bth },
    data() {
        return {
        }
    },
}

</script>
<style lang='scss' module>
.header {
  color: #666666;
  font-size: 32px;
  height: 100px;
  line-height: 100px;
  position: fixed;
  top: 0px;
  left: 0px;
  right: 0px;
  background: #fff url(../../images/bgimage.gif) center center no-repeat;
  background-size: auto 50%;
  z-index: 100;
  .left {
    font-size: 28px;
    height: 30px;
    line-height: 30px;
    margin: 17px 0 0 18px;
  }
  .btnDownload {
    float: right;
    font-size: 24px;
    border-width: 56px;
    line-height: 56px;
    min-width: 120px;
    padding: 0;
    border-radius: 4px;
    margin: 28px 24px 0 0;
  }
}
</style>
