<template>
  <VueSlickCarousel
    :arrows="true"
    :dots="true"
    :centerMode="true"
    :slidesToShow="3"
    :focusOnSelect="true"
    :initialSlide="2"
  >
    <div><img src="~assets/placeholder.png" /></div>
    <div>
      <img class="cont" src="~assets/DemoLorem.png" />
      <div class="overlay">
        <div class="text">No hidden content here</div>
      </div>
    </div>
    <div><img src="~assets/placeholder.png" /></div>
    <div><img src="~assets/placeholder.png" /></div>
  </VueSlickCarousel>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
// optional style for arrows & dots
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";

export default {
  name: "MyComponent",
  components: { VueSlickCarousel }
};
</script>
