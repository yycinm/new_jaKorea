<template>
  <div class="row">
    <swiper
    :spaceBetween="30"
    :centeredSlides="true"
    :autoplay="{
      delay: 2500,
      disableOnInteraction: false,
    }"
    :pagination="{
      clickable: true,
      el:'.swiper-pagination00',
      type : 'bullets',
     
    }"
    :navigation="true"
    :modules="modules"
    class="mySwiper03"
  >
    <swiper-slide v-if="tab == 1"
          v-for="item in edu01"
          :key="item"
          :class="{ edu01: (tab = 1) }"
          >
        <a :href="`http://${item.href}`"></a>
        <div class="conProTxt">

        <h3 v-html="item.title"></h3>
        <h4 v-html="item.subtitle"></h4>
        </div>
        <img :src="`./images/03eduProgram/${item.src}`" alt="" class="eduIm img-fluid d-md-block d-none">
    </swiper-slide>
    <swiper-slide v-if="tab == 2"
          v-for="item in edu02"
          :key="item"
          :class="{ edu02: (tab = 2) }">
        <a :href="`http://${item.href}`"></a>
         <div class="conProTxt">

        <h3 v-html="item.title"></h3>
        <h4 v-html="item.subtitle"></h4>
        </div>
        <img :src="`./images/03eduProgram/${item.src}`" alt="" class="eduIm img-fluid d-md-block d-none">
    </swiper-slide>
    <swiper-slide  v-if="tab == 3"
          v-for="item in edu03"
          :key="item"
          :class="{ edu03: (tab = 3) }">
        <a :href="`http://${item.href}`"></a>
           <div class="conProTxt">

        <h3 v-html="item.title"></h3>
        <h4 v-html="item.subtitle"></h4>
        </div>
        <img :src="`./images/03eduProgram/${item.src}`" alt="" class="eduIm img-fluid d-md-block d-none">
    </swiper-slide>
    <swiper-slide v-if="tab == 4"
          v-for="item in edu04"
          :key="item"
          :class="{ edu04: (tab = 4) }">
        <a :href="`http://${item.href}`"></a>
           <div class="conProTxt w-md-50">

        <h3 v-html="item.title"></h3>
        <h4 v-html="item.subtitle"></h4>
        </div>
        <img :src="`./images/03eduProgram/${item.src}`" alt="" class="eduIm img-fluid d-md-block d-none">
    </swiper-slide>
    <div v-for="(item,i) in eduProgram" :key="i" class="swiper-pagination00">
         <span class="swiper-pagination-bullet">222</span> 
        
    </div>
  </swiper> 
  </div>

</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/pagination";
import "swiper/css/navigation";

// import "./style.css";

// import required modules
import { Autoplay, Pagination, Navigation } from "swiper";
export default {
    components: {
    Swiper,
    SwiperSlide,
  },
    props:[
        "eduProgram",
        "edu01",
        "edu02",
        "edu03",
        "edu04",
        "tab"

    ]

}
</script>

<style lang="scss" scoped>
.swiper-slide{
 padding: 100px;height: 505px;display: flex;justify-content: center;align-items:center;width: 100%;
  .conProTxt{
    width: 100%;

  }
    h3{font-size: 35px;_background: red;font-weight: bolder;}
    h4{font-size: 18px;_background: pink;_width: 100%;padding: 10px 0;}
  }
  .eduIm{
    height: 100%;margin-left: 100px;
    }

</style>