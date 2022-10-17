<template>
  <div class="mSlide">
    <div class="container" style="width=1440px">
      <div class="row">
        <swiper
          :slidesPerView="1"
          :spaceBetween="30"
          :loop="true"
          :pagination="{
            clickable: true,
          }"
          :navigation="true"
          :modules="modules"
          class="mySwiper"
        >
          <swiper-slide v-for="(item, i) in mData" :key="i" class="swiperWrap">
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
            </div>
          </swiper-slide>
          <div class="next">ff</div>
          <div class="prev"></div>
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
  setup() {
    return {
      sData: sData,
      modules: [Pagination, Navigation],
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
}
.container {
  height: 745px;
  // width: 1440px !important;
  
  .row {
    height: 100%;
    width: 100%;
  }
    .mySwiper{
      width: 100%;height: 100%;background: #000;
     .swiperWrap{
        width: 100%;height: 100%;background: red;position: relative;
      }
    }
  video {
   
    height:736px;
    position: absolute;right: 0;
   
    background: green;
  }
  .mTxt {
    background: yellow;position: absolute;width: 100%;
    h2 {
      font-size: 66px;
    }
    span {
      font-weight: bold;
    }
    h3 {
      font-size: 18px;
    }
  }
}
</style>