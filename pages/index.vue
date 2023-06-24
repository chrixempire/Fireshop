<template>
 <div >
  <div class="container">
    <heroes/>
  <largeCardDisplay
  v-for="cardInfo in largeCardInfo"
  :key="cardInfo.id"
  :cardSection="cardInfo"
  />
  <smallCardDisplay
    v-for="cardInfo in smallCardSections"
    :key="cardInfo.id"
    :cardSection="cardInfo"
  />
  </div>
 </div>
</template>

<script>
import heroes from '~/components/heroes.vue'
import {largeCardSections, smallCardSections } from '@/assets/data.js'
import largeCardDisplay from '~/components/largeCardDisplay.vue'
import smallCardDisplay from '~/components/smallCardDisplay.vue'

export default {
  layout: 'appLayout',
  components: { heroes, largeCardDisplay, smallCardDisplay
  
  },
  name: 'IndexPage',
  data() {
    return{
      largeCardInfo : largeCardSections,
      smallCardSections 
    }
  }
}
</script>
