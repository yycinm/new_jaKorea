<template>
  <div class="container">
    <div class="row">
      <div class="col-12 col-md-4 bText mb-5">
        <p>국내외 여러기업이 동참하고 있습니다.</p>
        <h2 class="mb-5">JA KOREA 후원</h2>
        <div class="btn">
          <a href="#" class="text-center">

          자세히 보기
          </a>
          </div>
      </div>
      <div class="col-12 col-md-8 bIcon">
        <swiper
          :spaceBetween="30"
          :pagination="{
            clickable: true,
          }"
          :modules="modules"
          class="mySwiper03 mb-5"
        >
          <swiper-slide class="brands">
            <ul>
              <li v-for="(item, i) in support.slice(0, 3)" :key="i" class="threeM">
                <img :src="`images/09support/${item.src}`" alt="" />
              </li>
            </ul>
            <ul>
              <li v-for="(item, i) in support.slice(3, 6)" :key="i">
                <img :src="`images/09support/${item.src}`" alt="" />
              </li>
            </ul>
            <ul>
              <li v-for="(item, i) in support.slice(6, 9)" :key="i">
                <img :src="`images/09support/${item.src}`" alt="" />
              </li>
            </ul>
          </swiper-slide>
          <swiper-slide class="brands">
            <ul>
              <li v-for="(item, i) in support.slice(9, 12)" :key="i">
                <img :src="`images/09support/${item.src}`" alt="" />
              </li>
            </ul>
            <ul>
              <li v-for="(item, i) in support.slice(12, 15)" :key="i">
                <img :src="`images/09support/${item.src}`" alt="" />
              </li>
            </ul>
            <ul>
              <li v-for="(item, i) in support.slice(15, 18)" :key="i">
                <img :src="`images/09support/${item.src}`" alt="" />
              </li>
            </ul>
          </swiper-slide>
          <swiper-slide class="brands">
            <ul>
              <li v-for="(item, i) in support.slice(18, 21)" :key="i">
                <img :src="`images/09support/${item.src}`" alt="" />
              </li>
            </ul>
            <ul>
              <li v-for="(item, i) in support.slice(21, 24)" :key="i">
                <img :src="`images/09support/${item.src}`" alt="" />
              </li>
            </ul>
            <ul>
              <li v-for="(item, i) in support.slice(24, 27)" :key="i" class="mb-3">
                <img :src="`images/09support/${item.src}`" alt="" />
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
  props: ["support"],
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination],
    };
  },
};
</script>

<style lang="scss" scoped>
.container {margin-top: 100px;
  .bText {
    p{font-size: 17px;color:#285F74}
    h2{font-size: 45px;}
    .btn{height: 65px;
   
    line-height: 65px;
    padding: 5px 50px;
        background: #fff;
    box-shadow: 0 0 17px 6px rgb(0 0 0 / 9%);
  
    border-radius: 30px;
    color:#333;
    &:hover{transition:0.3s;
background-image: linear-gradient( -45deg,#00a0af,#00c0ca, #008b9c, #28708b,#28708b, #008b9c,#00c0ca,#00a0af)
    ;}
    &:hover a{
color: white;
    }

     a{transition:0.3s;
       display: flex;
    justify-content: space-between;
    align-items: center;width: 100%;height: 100%;
  
    }
  }}
  .bIcon {
    display: flex;justify-content: center;align-items:center;_width: 100%;height: 100%;
    ul {
      width: 100%;
      display: flex;
      justify-content: center;align-items:center;
     
      li {
        width: 164px;
        flex: 1 0 auto;
        height: 56px;
        transition: 0.3s;
        padding: 20px;
        img {
          width: 100%;
        }
      }
    }
  }
  .brands{ 
    ul{width: 100%;display: flex;justify-content: flex-end;align-items:center;
       .threeM{
        img{height: 55px;}
        
      }
      li{
       width:  calc(100%/3);;height: 90px;background: #dddddd;border-radius: 10px;padding: 20px 50px;
        margin-bottom: 10px;margin-right: 10px;
        display: flex;justify-content: center;align-items: center;
      }
    }
  }
}
</style>