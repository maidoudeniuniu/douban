<template>
  <div id="app">
    <header-component></header-component>
    <transition name="fade" mode="out-in">
      <router-view></router-view>
    </transition>
  </div>
</template>

<script>
import headerComponent from "./components/common/header.vue"
export default {
  name: 'comment',
  components:{
    headerComponent
  },
  data () {
    return {
      open: true
    }
  },
}
</script>


 