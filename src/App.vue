<template>
<header-top :menuList="menuList" :topMenu="topMenu"></header-top>
<main-slide :mData="mData"></main-slide>
<main-visual :notice="notice" :story="story" :news="news"></main-visual>

 
</template>

<script>
import mData from "@/data/01mainSlide";
import headerTop from "@/components/headerTop.vue";
import mainSlide from "@/components/mainSlide.vue";
import MainVisual from './components/MainVisual.vue';
import notice from "@/data/04notice";
import story from "@/data/05notice";
import news from "@/data/06new";
export default {
  data(){
    return{
      topMenu:[
        { src:"fa-solid fa-magnifying-glass",
          url:"#"},
        {src:"fa-solid fa-user-large",
          url:"https://www.jakorea.org/login.php"},
        {src:"fa-brands fa-facebook",
          url:"https://www.jakorea.org/login.php"},
        {src:"fa-brands fa-instagram",
          url:"https://www.jakorea.org/login.php"},
        {src:"fa-brands fa-youtube",
          url:"https://www.jakorea.org/login.php"},
        {src:"fa-solid fa-bars",
          url:"https://www.jakorea.org/login.php"},
       

      ],
      menuList: [
        {menu:"제이에이코리아",url:"https://www.jakorea.org/?p=2"},
        {menu:"투명경영",url:"#"},
        {menu:"교육사업",url:"#"},
        {menu:"기관소식",url:"#"},
        {menu:"후원하기",url:"#"},
      ],
      mData:mData,
      notice:notice,
      story:story,
      news:news,
     
    }
  },
  components:{
    headerTop,
    mainSlide,
    MainVisual,
  }

}
</script>

<style>
 @import url('@/assets/style.css');
 @import url('https://fonts.googleapis.com/css2?family=Nanum+Gothic+Coding&display=swap');
body{font-family: 'Nanum Gothic Coding', monospace;}
 
</style>
