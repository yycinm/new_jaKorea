<template>
  <div class="mSlide">
    <div class="container">
      <div class="row">
        <swiper 
        v-bind="swiperOptions"
        
          
          :pagination="{
            clickable: true,
          }"
          :navigation="true"
          :modules="modules"
          class="mySwiper"
        >
          <swiper-slide v-for="(item, i) in swiperView"
        :key="i"
          >
            <div
              class="video"
            >
              <!-- {{swiperView[0].subtitle}} -->
              <video autoplay muted loop playsinline style="" class="img-fluid">
                <source :src="`./images/01mainSlide/${item.mVideo}`" />
              </video>
              <div class="mTxt">
                <h2 v-html="item.mainTitle"></h2>
                <h3 v-html="item.subTitle"></h3>
              </div>
              <div class="btn text-center d-flex">
                <a href="#">
                  <h4 class="mx-4">

                  자세히 보기
                  </h4>
                  <img src="images/arrow.png" alt="" class="px-3">
                  </a>
                  
              </div>
            </div>
          </swiper-slide>
          <div class="swiper-button-next">
            111
            <img src="images/angle-left-solid.svg" alt="">
            <!-- <img src="images/angle-h_right-solid.svg" alt=""> -->
          </div>
          <div class="swiper-button-prev">
            222
              <img src="images/angle-right-solid.svg" alt="">
            <!-- <img src="images/angle-h_left-solid.svg" alt=""> -->
          </div>
        </swiper>
      </div>
      <!-- <div class="mVideo">
       
    </div> -->
    </div>
  </div>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/navigation";
import "swiper/css/pagination";

// import "./style.css";

// import required modules
import { Navigation, Pagination } from "swiper";
import sData from "@/data/01mainSlide";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      modules: [Navigation, Pagination],
      swiperView: sData,
      swiperOptions: {
        loop: true,
        navigation: {
          nextEl: '.mSlide .swiper-button-next',
						prevEl: '.mSlide .swiper-button-prev',
        },
        pagination: {
          type:'fraction',
          
        },
      },
    };
  },
  props: ["mData"],
};
// export default {
//     props:[
//         "mData",
//     ]
// }
</script>

<style lang="scss" scoped>
.mSlide{
  background: #E1F0F3;width: 1920px;height: 745px;
  .swiper-button-next{background: #000;position: absolute;top: 100px;z-index: 10;}
  .swiper-button-prev{background: #000;position: absolute;top:200px;}
}
.container {
  height: 745px;

  // width: 1440px !important;
  
  .row {
    height: 100%;
    max-width: 100%;
  
    .mySwiper{
      width: 100%;height: 100%;_background: #000;
     .swiperWrap{
        width: 100%;height: 100%;_background: red;position: relative;
      }
    }
  .video { 
   video{

     height:700px;
     position: absolute;right: -100px;bottom: 0;
    
     _background: green;
   }
 
  .mTxt {
    _background: yellow;position: absolute;width: 100%;
    top: 40%;transform:translateY(-50%);left: 3%;
    h2 {
      font-size: 63px;
      color:#285E76;
      font-weight: 300;

    }
    h3 {
      font-size: 18px;
      color:#285E76;
     line-height: 28px;
     font-weight: 600;

    }
  }
  .btn{
    height: 65px;
   
    line-height: 65px;
    background: #fff;
    position: absolute;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
    bottom: 25%;
    left: 3%;
    border-radius: 30px;
    a{
       display: flex;
    justify-content: space-between;
    align-items: center;
    h4{font-size: 17px;}
    }
   }
  }
  }
}
</style>