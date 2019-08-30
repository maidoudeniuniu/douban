<template>
  <div>
     <brand-component></brand-component>   
     <hot-component titile=""></hot-component>
     <hot-component titile=""></hot-component>
     <hot-component titile=""></hot-component>
     <hot-component titile=""></hot-component>
  </div>
</template>

<script>
import brandComponent from "./brand.vue"
import hotComponent from "./hot.vue"
export default {
  name: 'comment', 
  components:{
    brandComponent,
    hotComponent
  },
  data () {
    return {
      open: true
    }
  },
  computed: {
    comment () {
      return this.$store.state.items[this.id]
    }
  },
  methods: {
    pluralize: n => n + (n === 1 ? ' reply' : ' replies')
  }
}
</script>


<style lang="stylus" scoped>
 @import 'index.css'
</style>