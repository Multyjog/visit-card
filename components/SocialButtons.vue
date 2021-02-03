<template>
  <div class="social-buttons row mt-5">
    <h1 class="col-md-3">
      <a
        href="https://www.instagram.com/multyjog/?hl=ru"
        title="My Instagram"
        target="_blank"
        ><font-awesome-icon :icon="['fab', 'instagram']"
      /></a>
    </h1>
    <h1 class="col-md-3">
      <a
        href="https://www.facebook.com/semen.kotov.315/"
        title="My FaceBook"
        target="_blank"
        ><font-awesome-icon :icon="['fab', 'facebook-f']"
      /></a>
    </h1>
    <h1 class="col-md-3">
      <a
        href="https://stackoverflow.com/users/15061974/%d0%a1%d0%b5%d0%bc%d1%91%d0%bd-%d0%9a%d0%be%d1%82%d0%be%d0%b2"
        title="My StackOverflow"
        target="_blank"
        ><font-awesome-icon :icon="['fab', 'stack-overflow']"
      /></a>
    </h1>
    <h1 class="col-md-3">
      <a href="https://github.com/Multyjog" title="My GitHub" target="_blank"
        ><font-awesome-icon :icon="['fab', 'github']"
      /></a>
    </h1>
  </div>
</template>

<style scoped>
.social-buttons {
  text-align: -webkit-center;
}
.social-buttons a:hover {
  -webkit-transition: -webkit-transform 0.4s ease-out;
  transition: -webkit-transform 0.4s ease-out;
  transition: transform 0.4s ease-out;
  transition: transform 0.4s ease-out, -webkit-transform 0.4s ease-out;
  -webkit-transform: rotateZ(360deg);
  transform: rotateZ(360deg);
}
.social-buttons a {
  display: block;
  position: relative;
  width: 45px;
  font-size: 50px;
  text-align: center;
  text-decoration: none;
  color: white;
}
.social-buttons a:hover {
  text-decoration: none;
  color: rgba(17, 17, 17, 0.651);
}
</style>
