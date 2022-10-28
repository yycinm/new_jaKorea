<template>



  <div class="container">
    <div class="tabMenu row mb-5">
      <h2 class="col-12 col-md-4">JA 교육프로그램</h2>
      <div class="rowWrap col-12 col-md-6 conPro">
        <div class="row mb-3">
          <div class="col-3 tab" @click="tab = 1" :class="{ active: tab == 1 }">
           <h3> 진로취업</h3>
          </div>
          <div class="col-3 tab" @click="tab = 2" :class="{ active: tab == 2 }">
           <h3> 경제금융</h3>
          </div>
          <div class="col-3 tab" @click="tab = 3" :class="{ active: tab == 3 }">
          <h3>기업가정신</h3>
          </div>
          <div class="col-3 tab" @click="tab = 4" :class="{ active: tab == 4 }">
           <h3> 디지털 리터러시</h3>
          </div>
        </div>
      </div>
    </div>
    <conpro-sub
      :edu01="edu01"
      :edu02="edu02"
      :edu03="edu03"
      :edu04="edu04"
      :tab="tab"
      :eduProgram="eduProgram"
    ></conpro-sub>
  </div>
  <!-- <div class="conproBg d-md-block d-none"></div> -->
</template>

<script>
import ConproSub from "./ConproSub.vue";

export default {
  components: {
    ConproSub,
  },

  props: ["edu01", "edu02", "edu03", "edu04"],
  data() {
    return {
      tab: 1,
    };
  },
};
</script>

<style lang="scss" scoped>
.swiper-pagination00 {
  width: 50px;
  height: 50px;
  .swiper-pagination-bullet {
    width: 30px;
    height: 30px;
    background: green;
  }
  .swiper-pagination-bullet.swiper-pagination-bullet-active {
    background: pink;
  }
}
.tabMenu {
  display: flex;
  h2 {
    font-size: 50px;
    font-weight: bold;
  }
  .conPro{z-index: 10;
    .row{
      height: 100%;
      div{
        &:hover h3{
          font-weight: bold;
        }
      }
      div.active h3{
        border-bottom: 3px solid #285f74;
        font-weight: bold;

      }

    }
    
    h3{

      font-size: 20px;display: flex;justify-content: center;
      align-items: center;height: 100%;line-height: 100%;
      cursor: pointer;
    }
  }
}
.conproBg{
  width: 511px;height: 100%;border-radius: 100px 0 0 100px;
  background: #ccc;position: absolute;right: 0px; top: 0;opacity: 0.5;
}
.bbg{
  position: relative;
}
</style>