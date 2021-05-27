<template>
<div>
  <header-ing/>
  <banner-ing/>
 
  <about/>
  <flirting/>
  <servico-ing/>
  <contact/>
  <footer-ing/>

</div>

</template>
<style lang="scss">
@import '../css/app.scss';
</style>

<script>

import HeaderIng from 'src/components/ingles/HeaderIng.vue'
import BannerIng from '../components/ingles/bannerIng.vue'
import Flirting from 'src/components/ingles/Flirting.vue'
import ServicoIng from 'src/components/ingles/servicoIng.vue'
import Contact from 'src/components/ingles/Contact.vue'
import FooterIng from 'src/components/ingles/FooterIng.vue'


export default {
  components:{
    
    HeaderIng,
    BannerIng,
    SevicoIng,
    Flirting,
    ServicoIng,
    Contact,
    FooterIng
  }
 
}
</script>
