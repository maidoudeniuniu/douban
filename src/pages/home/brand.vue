<template>
  <div class="brandBox">
    <div class="w1200 relativebox" style="height:305px">
     <div style="margin-left:570px;">
         <div style="padding-top:70px;font-size:20px;margin-bottom:20px">APP6.0</div> 
         <dnowapp-component></dnowapp-component>       
     </div>
     <div class="loginbox">       
        <login-component @telcode="telcode"></login-component>
      </div>
    </div>
  </div>
</template>

<script>
import loginComponent from "../../components/login/minlogin.vue"
import dnowappComponent from "../../components/dwonapp.vue"
export default {
  name: 'comment',
  props: ['id'],
  components:{
    loginComponent,
    dnowappComponent
  },
  data () {
    return {
      open: true
    }
  },
  methods:{
    telcode (e) {
      console.log(e)
    }
  }   
}
</script>

<style lang="stylus" scoped>
.brandBox {
  background: url('/public/common/index_bg.jpg') no-repeat;
  background-size: contain;
  background-position: -webkit-calc(50% - 305px) top;
  background-position: calc(50% - 305px) top;
  background-repeat: no-repeat;
  background-color: #edf4ed;
  min-height: 305px;
}
.loginbox{
  position absolute;
  top:0;
  right 0
  bottom 0
}
</style>