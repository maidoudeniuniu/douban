<template>
  <div>
     <div class="doubanxieyi gary">请仔细阅读 豆瓣使用协议、隐私政策</div>
     <div class="loginList">
       <div class="itemList">
          <input type="text" placeholder="手机号" v-model="tel">  
       </div>
       <div class="itemList">
         <input type="text" placeholder="登录密码" v-model="password">         
       </div>
       <div class="itemList">
         <Button type="success" long @click="login">登录</Button>
       </div>
        <div class="mb10 clearfix">
         <span class="fl">下次自动登录</span>
         <span class="fr">海外手机登录</span>
       </div>
     </div>
  </div>
</template>

<script> 
let sendData;
export default {
  name: 'comment', 
  components:{  
  },
  data () {
    return {      
      tel:"",
      password:"",     
    }
  },
  mounted () {
   
  },
  methods:{
    login () {       
       alert("登录成功")
    }, 
  }   
}
</script>

<style lang="stylus" scope="">
.qrcode{
  color #06c
  cursor pointer
}
.doubanxieyi{
  padding 10px 0;
} 
.itemList{
  margin-bottom 10px
  position relative
  input{
    border #ddd 1px solid
    height 35px
    width 100%
    text-indent 1em
  }
  .qrcode{
    position absolute
    top 0
    right 10px
    height 35px
    line-height 35px
    color #06c
  }
}
</style>