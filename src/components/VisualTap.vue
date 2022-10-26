<template>

  <div class="row mb-5">
    <div>
      <swiper v-bind="swiperOptions01" modules="modules" class="mySwiper01">
        <swiper-slide
          v-if="tab == 1"
          v-for="item in notice"
          :key="item"
          :class="{ notice: (tab = 1) }"
        >
          <h4>{{ item.name }}</h4>
          <h3>{{ item.title }}</h3>
          <h5>{{ item.subtitle }}</h5>
        </swiper-slide>
        <swiper-slide
          v-if="tab == 2"
          v-for="item in story"
          :key="item"
          :class="{ story: (tab = 2) }"
        >
          <h4>{{ item.name }}</h4>
           <h3>{{ item.title }}</h3>
          <h5>{{ item.subtitle }}</h5>
        </swiper-slide>
        <swiper-slide
          v-if="tab == 3"
          v-for="item in news"
          :key="item"
          :class="{ news: (tab = 3) }"
        >
          <h4>{{ item.name }}</h4>
           <h3>{{ item.title }}</h3>
          <h5 v-html="item.subtitle"></h5>
        </swiper-slide>
      </swiper>
    </div>
  </div>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/pagination";

// import "./style.css";

// import required modules
import { Pagination } from "swiper";
export default {
  props: ["notice", "story", "news", "tab"],
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination],
      swiperOptions01: {
        slidesPerView: "3",
        spaceBetwee: "30",

        pagination: {
          clickable: true,
        },
        breakpoints: {
        
          500: {
            slidesPerView: 2,  //브라우저가 768보다 클 때
            spaceBetween: 40,
          },
          1024: {
            slidesPerView: 3,  //브라우저가 1024보다 클 때
            spaceBetween: 50,
          },
      }
      }
    }
  }
};
</script>

<style lang="scss" scoped>
.mySwiper01 {
  display: flex;
  justify-content: space-between;
  align-items: center;

  h4 {
    font-size: 13px;
    background: #000;
    color: white;
    border-radius: 20px;
    height: 32px;
    text-align: center;
    line-height: 32px;
    width: 25%;
    margin-bottom: 20px;
  }
  h3{
    font-size: 24px;
  }
  h5{
    font-size: 18px;
    
  }
.swiper-slide {text-overflow: ellipsis;
    overflow: hidden;
  
padding: 20px;
}
}
</style>