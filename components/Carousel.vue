<template>
  <div class="carousel">
    <swiper ref="mySwiper" :options="swiperOptions">
      <swiper-slide><img src="../static/350x300.png" alt=""></swiper-slide>
      <swiper-slide><img src="../static/350x300.png" alt=""></swiper-slide>
      <swiper-slide><img src="../static/350x300.png" alt=""></swiper-slide>
      <swiper-slide><img src="../static/350x300.png" alt=""></swiper-slide>
      <swiper-slide><img src="../static/350x300.png" alt=""></swiper-slide>
      <swiper-slide><img src="../static/350x300.png" alt=""></swiper-slide>
      <swiper-slide><img src="../static/350x300.png" alt=""></swiper-slide>

      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
    <div class="roulette" style="display:none;" :roulette="option"> 
      <img src="../static/350x300.png" />
      <img src="../static/350x300.png" />
      <img src="../static/350x300.png" />
      <img src="../static/350x300.png" />
      <img src="../static/350x300.png" />
    </div> 
  </div>
</template>
<style scoped>
.carousel {
  width: 70%;
  margin: 20px auto;
}
.inv {
  display: none;
}
</style>
 
<script>
  import { Swiper, SwiperSlide, directive } from 'vue-awesome-swiper'
  import 'swiper/swiper-bundle.css'

  export default {
    data() {
      return {
        swiperOptions: {
          slideToClickedSlide:'true',
          grabCursor: 'true',
          loop: true,
          effect: 'coverFlow',
          slidesPerView: '3',
          centerSlides: 'true',
          updateOnWindowResize:'true',
        },
        option: {
          speed : 10,
          duration : 3,
          stopImageNumber : 0,
          startCallback : function() {
            console.log('start');
          },
          slowDownCallback : function() {
            console.log('slowDown');
          },
          stopCallback : function($stopElm) {
            console.log('stop');
          }
        }
      }
    },
    name: 'MyComponent',
    components: { 
      Swiper,
      SwiperSlide
    },
    directives: {
    swiper: directive
    }
  }
</script> 

