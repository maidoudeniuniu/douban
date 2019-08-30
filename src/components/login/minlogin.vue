<template>
  <div class="loginbox">     
    <div class="loginHd">
      <div @click="tab(1)" :class="{ative:show==1}">短信登录／注册</div>
      <div @click="tab(2)" :class="{ative:show==2}">密码登录</div>
    </div>
    <div class="loginBd">
      <div v-if="show==1">
        <reg-component></reg-component> 
      </div>
      <div v-if="show==2">
        <login-component></login-component>  
      </div>
    </div>
    <div>
      第三方登录:微信,支付宝
    </div>
  </div>
</template>

<script> 
import regComponent from './reg.vue'
import loginComponent from './login.vue'
export default {
  name: 'comment',
  components:{
    regComponent,
    loginComponent
  },
  data () {
    return {
      open: true,
      show:1
    }
  },
  mounted () {



  },   
  methods: {
    tab (e) {
      this.show = parseInt(e)
    }
  },
}
</script>


<style lang="stylus">
.loginbox{
  width 300px 
  height 100%
  .loginHd{
    height 60px;
    line-height 60px;
    float left;
    width 100%
    border-bottom #eee 1px solid;
    cursor pointer
    div.ative{
      color #000
      font-weight bold
      border-bottom #000 1px solid      
    }
    div{
      float left
      width 50%
      text-align center
    }
  }
  .loginBd{
    float left;
    width 100%
  }
}
</style>
