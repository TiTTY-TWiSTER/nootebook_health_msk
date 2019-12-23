<template>
  <div id="app">
      <first-screen></first-screen>
      <second-screen></second-screen>
      <third-screen></third-screen>
      <four-screen></four-screen>
      <five-screen></five-screen>
      <six-screen></six-screen>
      <footer-app></footer-app>
      <div class="arrow">
          <img src="/assets/app/build/zdoroviya_dnevnik_msk/arrow.png" alt="" @click='moveUp'>
      </div>
  </div>
</template>

<script>
import First from './first_screen.vue'
import Second from './second-screen.vue'
import Third from './third.vue'
import Four from './four.vue'
import Five from './five.vue'
import Six from './six.vue'
import Footer from './footer.vue'

import JQuery from 'jquery'
  let $ = JQuery

export default {
  name: 'app',
  data () {
    return {
     
    }
  },
  components:{
    'first-screen':First,
    'second-screen':Second,
    'third-screen':Third,
    'four-screen':Four,
    'five-screen':Five,
    'six-screen':Six,
    'footer-app':Footer
  },
  mounted(){
    this.arrow()
  },
  methods:{
    arrow(){
        $(window).scroll(function(){
          var scroll = $(window).scrollTop()
          if (scroll > 850) {
            $('.arrow').css({display:'block'})
          }
          if(scroll < 850){
            $('.arrow').css({display:'none'})
          }
        })
    },
    moveUp(){
        $('body,html').animate({scrollTop: 0},700);
    },
  }
}
</script>

<style>
  body{
    margin:0;
    overflow-x: hidden;
    font-family: 'Open Sans', sans-serif;
  }
  .arrow{    
    display:none;    
    position:fixed;
    bottom:5%;
    right:3%;
  }
  .arrow img{
    width:50px;
    cursor:pointer;
  }
  .arrow img:hover{
   transform:scale(1.1);
  }
</style>
