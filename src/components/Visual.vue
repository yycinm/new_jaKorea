<template>

  <div class="container mb-5">
    <div class="row visual">
       
    <visual-recruit :Vnotice="Vnotice"></visual-recruit>
    <visual-result :result="result"></visual-result>
    </div>
    

    
</div>
</template>

<script>
import VisualRecruit from './VisualRecruit.vue'
import VisualResult from './VisualResult.vue'

import Vnotice from '@/data/07notice'
import result from '@/data/08result'
export default {
  components: { 
    VisualRecruit,
    VisualResult,

   },

   data(){
    return{
        Vnotice:Vnotice,
        result:result
    }
   }

}
</script>


  <style lang="scss" scoped>



</style>