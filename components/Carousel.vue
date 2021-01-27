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
          effect: 'cube',
          slidesPerView: '3',
          centerSlides: 'true',
          updateOnWindowResize:'true',
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

