<template>
  <div class="mSlide">
  <div class="container">
    <swiper :pagination="true" :modules="modules" class="mySwiper">
    <swiper-slide>Slide 1</swiper-slide><swiper-slide>Slide 2</swiper-slide
    ><swiper-slide>Slide 3</swiper-slide><swiper-slide>Slide 4</swiper-slide
    ><swiper-slide>Slide 5</swiper-slide><swiper-slide>Slide 6</swiper-slide
    ><swiper-slide>Slide 7</swiper-slide><swiper-slide>Slide 8</swiper-slide
    ><swiper-slide>Slide 9</swiper-slide>
  </swiper>
    <!-- <div class="mVideo">
        <video  v-for="(item,i) in mData" :key="i" autoplay controls>
              <source :src="item.mVideo" type="video/mp4">
        </video>
    </div> -->
  </div>

</div>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/pagination";

import "./style.css";

// import required modules
import { Navigation, Pagination } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination, Navigatio],
    };
  },
};
// export default {
//     props:[
//         "mData",
//     ]
// }
</script>

<style lang="scss">
.container{
  height: 745px;width: 100%;background: pink;
  .mVideo{
width: 500px;
  }
 }
</style>