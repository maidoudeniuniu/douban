<template>
  <div class="tipapp">
    <div class="fl mr10">
      <i-button type="success">下载APP</i-button>
    </div>
    <div class="fl relativebox qrcodeItem">
      <span class="qrcodeborder">
        <img src="/public/common/icon_qrcode.png" alt="" width="28" height="28">
      </span>
      <div class="qrcodeshow" v-if="show">
        <img src="https://img3.doubanio.com/f/sns/1cad523e614ec4ecb6bf91b054436bb79098a958/pics/sns/anony_home/doubanapp_qrcode.png" width="160" height="160">
        <div>iOS / Android 扫码直接下载</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'comment', 
  data () {
    return {
      show: false
    }
  },
  mounted () {
    let _this = this
     $(".qrcodeItem").hover(()=>{
       _this.show = true
     },()=>{       
       _this.show = false
     }) 
  },  
}
</script>

<style lang="stylus">
 .qrcodeborder{
   border: #48aa0d 1px solid;
   overflow hidden 
   height 30px   
   float left;
 }

 .qrcodeshow{
   position absolute;
   top 0
   left 0
   background #ffffff
   padding 10px
   border-radius 0 5px 5px 5px 
   div{
     color #999;
     padding 10px 0
     text-align center
   }
 }
</style>