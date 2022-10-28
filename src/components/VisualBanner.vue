<template>
  <div class="container">
    <div class="row">
        <div class="col-12 col-md-4 bg-info bText">
            <p>국내외 여러기업이 동참하고 있습니다.</p>
            <h2>JA KOREA 후원</h2>
            <div class="btn">
                
            </div>
        </div>
        <div class="col-12 col-md-8 bIcon">
            <swiper
    :spaceBetween="30"
    :pagination="{
      clickable: true,
    }"
    :modules="modules"
    class="mySwiper03"
  >
    <swiper-slide> 
         <ul>
                <li v-for="(item,i) in support.slice(0, 3)" :key="i">
                    <img :src="`images/09support/${item.src}`" alt="">
                </li>
                
        </ul>
         <ul>
                <li v-for="(item,i) in support.slice(3, 6)" :key="i">
                    <img :src="`images/09support/${item.src}`" alt="">
                </li>
                
        </ul>
         <ul>
                <li v-for="(item,i) in support.slice(6, 9)" :key="i">
                    <img :src="`images/09support/${item.src}`" alt="">
                </li>
                
        </ul>
    </swiper-slide>
    <swiper-slide> 
         <ul>
                <li v-for="(item,i) in support.slice(9, 12)" :key="i">
                    <img :src="`images/09support/${item.src}`" alt="">
                </li>
                
        </ul>
         <ul>
                <li v-for="(item,i) in support.slice(12, 15)" :key="i">
                    <img :src="`images/09support/${item.src}`" alt="">
                </li>
                
        </ul>
         <ul>
                <li v-for="(item,i) in support.slice(15, 18)" :key="i">
                    <img :src="`images/09support/${item.src}`" alt="">
                </li>
                
        </ul>
    </swiper-slide>
    <swiper-slide> 
         <ul>
                <li v-for="(item,i) in support.slice(18, 21)" :key="i">
                    <img :src="`images/09support/${item.src}`" alt="">
                </li>
                
        </ul>
         <ul>
                <li v-for="(item,i) in support.slice(21, 24)" :key="i">
                    <img :src="`images/09support/${item.src}`" alt="">
                </li>
                
        </ul>
         <ul>
                <li v-for="(item,i) in support.slice(24, 27)" :key="i">
                    <img :src="`images/09support/${item.src}`" alt="">
                </li>
                
        </ul>
    </swiper-slide>
    
  </swiper>
           
        </div>
    </div>
  </div>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/pagination";


// import required modules
import { Pagination } from "swiper";

export default {
    props:[
        "support"
    ],
     components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination],
    };
  },
    

}
</script>

<style lang="scss" scoped>
.container{
    .bText{

    }
    .bIcon{
    
        ul{
            width: 100%;display: flex;
            li{ width: 30%;flex: 1 0 auto;
            transition: .3s;padding: 10px;}
        }
    }
}

</style>