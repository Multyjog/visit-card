<template>
  <div>
    <div>
      <img class="logofield hidden" src="~assets/rostok.png" alt="LOGOTITLE" />
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    let showImg = function() {
      img.classList.remove("hidden");
    };
    var img = this.$el.querySelector("img");
    img.addEventListener("load", showImg);
    if (img.complete) {
      showImg();
    }
  }
};
</script>
<style>
.hidden {
  opacity: 0 !important;
}

.logofield {
  max-width: 100%;
  width: 100%;
  height: auto;
  max-height: 600px;
  transition: opacity 0.15s ease-in-out;
  opacity: 1;
}
</style>
