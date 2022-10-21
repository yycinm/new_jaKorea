<template>
<div class="container sosic">
<div class="tabMenu">

  <h2>JA 기관소식</h2>
  <div class="rowWrap">

  <div class="row mb-3">
    <div class="col-4 tab" @click="tab=1" :class="{active:tab==1}" >공지사항</div>
    <div class="col-4 tab" @click="tab=2" :class="{active:tab==2}">스토리</div>
    <div class="col-4 tab" @click="tab=3" :class="{active:tab==3}">언론보도</div>
  </div>
  </div>
</div>
  <visual-tap :notice="notice" :story="story" :news="news" :tab="tab"></visual-tap>
  
</div>
</template>

<script>
import VisualTap from './VisualTap.vue'
export default {
  components: { VisualTap },

  props:[
    "notice",
    "story",
    "news",
    
  ],
  data(){
    return{
        tab:1
    }
  }

}
</script>

<style lang="scss">
.container.sosic{
   height: 557px;
.tabMenu{width: 100%;
  
    .row{width: 300px;
    display: flex;justify-content: center;
    align-items: center;
    height: 50px;line-height: 50px;
    text-align: center;
    }
 h2{font-size: 45px;font-weight: 600;margin-right: 50px;height: 100px;line-height: 100px;}

}
    }
</style>