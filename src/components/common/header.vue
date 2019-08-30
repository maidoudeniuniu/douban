<template>
   <header class="headerNav">
     <div class="headerNavBox">
       <div class="headerLogin" @click="logon" title="豆瓣"></div>
        <div class="headerNavList">
          <div class="fl headerInput">
            <input type="text" placeholder="书籍、电影、音乐、小组、小站、成员">
          </div>
          <div class="Navlist fl">
            <ul>
              <li v-for="item in navList" >
                <a :href="item.url" target="_blank" :class="item.className">
                  {{item.name}}
                </a>
              </li>
            </ul>
          </div>
       </div>
     </div>
   </header>
</template>
<script>
export default {
  name: 'comment', 
  data () {
    return {
      navList:[
        {
          name:"读书",
          className:"lnk-book",
          url:"/book"
        },
        {
          name:"电影",
          className:"lnk-movie",
          url:"/movie"
        },
        {
          name:"音乐",
          className:"lnk-music",
          url:"/music"
        },
        {
          name:"小组",
          className:"lnk-book",
          url:"/book"
        },
        {
          name:"同城",
          className:"lnk-events",
          url:"/events"
        },
        {
          name:"FM",
          className:"lnk-fm",
          url:"/fm"
        },        
        {
          name:"豆品",
          className:"lnk-market",
          url:"/market"
        }, 
      ]
    }
  },  
}
</script>
<style lang="stylus">
  .headerNav{
    width: 100%;
    background: #fff;
    overflow: hidden;
    padding:30px 0;
    .headerNavBox{
      width 1200px
      margin 0 auto
      overflow hidden
      .headerLogin{
       float left
       width 260px
       height 35px
       background url("/public/common/logo_db.png") no-repeat
      }
      .headerNavList{
        display block
        margin-left:200px;
        overflow hidden
      }
    }  
    .headerInput{
      width 300px
      margin-right 20px
      input{
        border #ddd 1px solid
        height 30px;
        width 100%
      }      
    }
    .Navlist{
      float left
      ul{
        li{
          float left;
          margin 0 0 0 20px
          a{
            display: inline-block;
            *display: inline;
            zoom: 1;
            width: 40px;
            height: 20px;
            overflow: hidden;
            margin: 0;
            line-height: 20em;
            outline: none;
            vertical-align: middle;
            background url("/public/common/anony_nav_logo.png") no-repeat
          }
        }
        li .lnk-book {
            background-position: 0 0
        }

        li .lnk-movie {
            background-position: -60px 0
        }

        li .lnk-music {
            background-position: -120px 0
        }

        li .lnk-group {
            background-position: -180px 0
        }

        li .lnk-fm {
            background-position: -241px 0
        }

        li .lnk-events {
            background-position: -299px 0
        }

        li .lnk-market {
            width: 42px;
            background-position: -421px 0
        }

        li .lnk-shijian {
            margin-bottom: 1px;
            background: transparent url(/f/sns/b474dd402e4293943146a4789de3dae88ec96636/pics/sns/anony_home/ic_shijian_home_nav.png) no-repeat 100% 100%;
            background-image: -webkit-image-set(url(/f/sns/b474dd402e4293943146a4789de3dae88ec96636/pics/sns/anony_home/ic_shijian_home_nav.png) 1x, url(/f/sns/74745beec69da53ac959a9bcc4e1e66f852ba2e8/pics/sns/anony_home/ic_shijian_home_nav@2x.png) 2x);
            background-image: -moz-image-set(url(/f/sns/b474dd402e4293943146a4789de3dae88ec96636/pics/sns/anony_home/ic_shijian_home_nav.png) 1x, url(/f/sns/74745beec69da53ac959a9bcc4e1e66f852ba2e8/pics/sns/anony_home/ic_shijian_home_nav@2x.png) 2x);
            background-image: -ms-image-set(url(/f/sns/b474dd402e4293943146a4789de3dae88ec96636/pics/sns/anony_home/ic_shijian_home_nav.png) 1x, url(/f/sns/74745beec69da53ac959a9bcc4e1e66f852ba2e8/pics/sns/anony_home/ic_shijian_home_nav@2x.png) 2x);
            background-image: -o-image-set(url(/f/sns/b474dd402e4293943146a4789de3dae88ec96636/pics/sns/anony_home/ic_shijian_home_nav.png) 1x, url(/f/sns/74745beec69da53ac959a9bcc4e1e66f852ba2e8/pics/sns/anony_home/ic_shijian_home_nav@2x.png) 2x);
            background-size: cover
        }
      } 
    }
  }
 </style>