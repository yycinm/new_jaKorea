<template>
<header-top :menuList="menuList" :topMenu="topMenu"></header-top>
<main-slide :mData="mData"></main-slide>
<main-content :iconbanner="iconbanner"></main-content>
<content-program :edu01="edu01" :edu02="edu02" :edu03="edu03" :edu04="edu04"></content-program>

<content-count></content-count>
<main-visual :notice="notice" :story="story" :news="news"></main-visual>
<visual></visual>
<visual-vedio></visual-vedio>
<visual-banner :support="support"></visual-banner>
<visual-subscribe></visual-subscribe>
<footer-banner></footer-banner>

 
</template>

<script>
import mData from "@/data/01mainSlide";
import headerTop from "@/components/headerTop.vue";
import mainSlide from "@/components/mainSlide.vue";
import MainVisual from './components/MainVisual.vue';

import iconbanner from '@/data/02iconBanner';
import eduProgram from '@/data/03eduProgram';
import edu01 from '@/data/edu01';
import edu02 from '@/data/edu02';
import edu03 from '@/data/edu03';
import edu04 from '@/data/edu04';
import support from '@/data/09support';

import notice from "@/data/04notice";
import story from "@/data/05notice";
import news from "@/data/06new";
import MainContent from './components/MainContent.vue';
import ContentProgram from './components/ContentProgram.vue';
import ContentCount from './components/ContentCount.vue';
import Visual from './components/Visual.vue';
import VisualVedio from './components/VisualVedio grid.vue';
import VisualBanner from './components/VisualBanner.vue';
import VisualSubscribe from './components/VisualSubscribe.vue';
import FooterBanner from './components/FooterBanner.vue';






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
      iconbanner:iconbanner,
      eduProgram:eduProgram,
      edu01:edu01,
      edu02:edu02,
      edu03:edu03,
      edu04:edu04,
      support:support,
     
    }
  },
  components:{
    headerTop,
    mainSlide,
    MainVisual,
    ContentCount,
    MainContent,
    ContentProgram,
    Visual,
    VisualVedio,
    VisualBanner,
    VisualSubscribe,
    FooterBanner,


  }

}
</script>

<style>
 @import url('@/assets/style.css');
 @import url('https://fonts.googleapis.com/css2?family=Nanum+Gothic+Coding&display=swap');
body{font-family: 'Nanum Gothic Coding', monospace;}
 
</style>
