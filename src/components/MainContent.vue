<template>
  <div class="container mb-5">
    
    <div class="row">
        <ul class="iBan quick-li col-md col-6">
            <li v-for="(item,i) in iconbanner" :key="i" class="iconBa">
                <a :href="`http://${item.href}`">
                <img :src="`./images/02iconBanner/${item.src}`" alt="">
                <div class="iconTxt">
                    <h5 v-html="item.title" class="text-center">
                        </h5>
                   <h6 v-html="item.subtitle" class="text-center"></h6>
                </div>
                </a>
            </li>
        </ul>
        
    </div>
  </div>
</template>

<script>
export default {
 
    props:[
        "iconbanner"
    ]

}
</script>

<style lang="scss" scoped>

    .iBan{
        width: 1290px;height: 254px;display: flex;margin: 0 auto;
        li{
            width: calc( 100% / 5 );height: 100%;
            display: flex;justify-content: center;align-items: center;
            img{
                width: 100%;height: 135px;
                display: flex;justify-content: center;align-items: center;
            }
            .iconTxt{
                width: 100%;height: 100%;
                h5{font-size: 18px;font-weight: bold;
                width: 100%;display: flex;justify-content: center;align-items: center;}
                h6{font-size: 15px;
                display: flex;justify-content: center;align-items: center;}
            }
        }
    }
</style>