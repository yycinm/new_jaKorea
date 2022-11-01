<template>
  <div class="container">
    <div class="row">
      <div class="col-12 col-md-4 bText">
        <p>국내외 여러기업이 동참하고 있습니다.</p>
        <h2>JA KOREA 후원</h2>
        <div class="btn">자세히 보기</div>
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
    background: #fff;
    position: absolute;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
    bottom: 25%;
    left: 3%;
    border-radius: 30px;
    color:#333

    }
  }
  .bIcon {
    ul {
      width: 100%;
      display: flex;
     
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
    ul{
       .threeM{
        img{height: 55px;}
        
      }
      li{
        width: 275px;height: 90px;background: #dddddd;border-radius: 10px;padding: 20px 50px;
        margin-bottom: 10px;margin-right: 10px;
        display: flex;justify-content: center;align-items: center;
      }
    }
  }
}
</style>