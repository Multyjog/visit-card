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
  text-align: center;
}
a {
  text-decoration: none;
  color: white;
}
</style>
