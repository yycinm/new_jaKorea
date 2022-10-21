<template>
   <div class="container mb-3">
    <div class="navbar">
      <a href="#">
        <img src="images/logo.svg" alt="" class="w-100 h-100">
      </a>
      <div class="nav">
        <ul class="ms-auto tMenu">
            <li  v-for="(item,i) in topMenu" :key="i">
                 <a :href="item.url"><i :class="`${topMenu[i].src}`"></i></a>
            </li>
        </ul>
        <ul class="mainmenu">
          <li  v-for="(item,i) in menuList" :key="i">
            <a :href="item.url">{{menuList[i].menu}}</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    props:[
        "menuList",
        "topMenu"
        
    ]
}
</script>

<style lang="scss">
 .nav{width: 700px;height: 50px;
 ul{

     width: 100%;height: 100%;display: flex;
     li{width: calc(100% / 5);
        display: flex;justify-content: center;align-items: center;}
}
.tMenu{
 width: 200px;height:20px;

}
 }
 
</style>