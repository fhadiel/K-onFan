<template lang="html">
  <div id="footHolder">
    <a target='_blank' href="http://www.tbs.co.jp/anime/k-on/index-j.html"><img class="iconPic" src="../assets/element/k-on.png" alt=""></a>
    <div class="textHolder">
      开源技术支持 :
      <div><a target='_blank' href="https://cn.vuejs.org/">Vue.js&nbsp &nbsp</a></div>
      <div><a target='_blank' href="https://github.com/ElemeFE/element">Element.UI&nbsp &nbsp</a></div>
      <div><a target='_blank' href="https://github.com/MoePlayer/vue-aplayer">MoePlayer&nbsp &nbsp</a></div>
      <div><a target='_blank' href="http://fontawesome.dashgame.com/">FontAwesome</a></div>
    </div>
    <popover class="bigScreen" title='内容助力感谢' :content='content'></popover>
  </div>
</template>

<script>
import popover from '@/components/general_popover.vue'
export default {
  components:{
    popover,
  },
  data(){
    return {
      content: [
        {
          id: 1,
          name: 'Mio秋山澪_',
          info: 'BILIBILI主页',
          link: 'http://space.bilibili.com/13856907/#/dynamic',
        },
        {
          id: 2,
          name: '我捏起来_超软的',
          info: 'BILIBILI主页',
          link: 'http://space.bilibili.com/14698426/#/dynamic',
        },
        {
          id: 3,
          name: '放課後-TeaTime',
          info: 'BILIBILI主页',
          link: 'http://space.bilibili.com/36909978/#/dynamic',
        },
        {
          id: 4,
          name: 'guillermocs18',
          info: 'Reddit主页',
          link: 'https://www.reddit.com/user/guillermocs18',
        },
      ]
    }

  },
}
</script>

<style scoped>
  a {
    text-decoration: none;
    color: #F56C6C;
    target: _blank;
  }
  #footHolder {
    background-color: #DCDFE6;
    height: 66px;
    text-align: center;
    position: relative;
  }
  .iconPic {
    height: 70%;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
  .textHolder {
    position: absolute;
    left: 100px;
    top: 0;
    height: 100%;
    color: #606266;
  }
  .textHolder > div {
    display: inline-block;
    line-height: 66px;
  }
  @media only screen and (max-width:600px) {
    * {
      box-sizing: border-box;
    }
    a {
      color: white;
    }
    .textHolder {
      display: flex;
      flex-wrap: wrap;
      height: 2rem;
      line-height: 2rem;
      position: absolute;
      top: -2rem;
      left: 0;
      width: 100%;
    }
    .textHolder > div {
      flex-grow: 1;
      line-height: 2rem;
    }
    .bigScreen {
      display: none;
    }
    .iconPic {
      height: 70%;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }
  }
</style>
