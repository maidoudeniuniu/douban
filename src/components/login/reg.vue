<template>
  <div>
     <div class="doubanxieyi gary">请仔细阅读 豆瓣使用协议、隐私政策</div>
     <div class="loginList">
       <div class="itemList">
          <input type="text" placeholder="手机号" v-model="tel">  
       </div>
       <div class="itemList">
         <input type="text" placeholder="验证码" v-model="code"> 
         <span class="qrcode" @click="send">{{codeTitle}}</span>
       </div>
       <div class="itemList">
         <Button type="success" long>登录</Button>
       </div>
       <div class="mb10 clearfix">
         <span class="fl">下次自动登录</span>
         <span class="fr">收不到验证码</span>
       </div>
     </div>
  </div>
</template>

<script>
import loginComponent from "../../components/login/minlogin.vue"
import dnowappComponent from "../../components/dwonapp.vue"
let sendData;
export default {
  name: 'comment',
  props: ['id'],
  components:{
    loginComponent,
    dnowappComponent
  },
  data () {
    return {
      codeTitle:"发送验证码",
      tel:"",
      code:"",
      num:60
    }
  },
  mounted () {
   
  },
  methods:{
    send () {       
      if(this.codeTitle == "发送验证码"){            
          this.sendCodeItem()
      } 
    },
    sendcode () {  
      if(this.num>=1){
        this.num = this.num - 1
        this.codeTitle = "已发送"+ this.num
      }else{
        this.num = 60
        this.codeTitle = "发送验证码"
         clearInterval(sendData)
      }    
    },      
    sendCodeItem (e) {
      let _this = this    
       //这里是发送短信的
      sendData = setInterval(() => {
          _this.sendcode()
        }, 1000); 
    }
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