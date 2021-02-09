<template>
  <div class="mb-5 container">
    <h1 class="logo mb-5">My projects</h1>
    <div class="row demos">
      <div class="col-md-4">
        <img class="empty" src="~assets/placeholder.png" />
      </div>
      <div class="col-md-4 cont">
        <img src="~assets/DemoLorem.png" />
        <div class="overlay">
          <div class="text">
            <h3>Super Lorem</h3>
            <p class="mt-2">
              Easy example of store counter with little JS &amp; API features.
            </p>
          </div>
          <a
            href="https://multyjog.github.io/vuesite2/"
            target="_blank"
            class="overlayButton"
            >Go look at me</a
          >
        </div>
      </div>
      <div class="col-md-4">
        <img class="empty" src="~assets/placeholder.png" />
      </div>
    </div>
  </div>
</template>

<style scoped>
.overlayButton {
  display: inline-block;
  padding: 15px 25px;
  font-size: 20px;
  font-weight: bold;
  cursor: pointer;
  text-align: center;
  text-decoration: none;
  outline: none;
  color: rgb(0, 0, 0);
  background-color: #e0dd11;
  border: none;
  border-radius: 15px;
  box-shadow: 0 9px rgb(78, 78, 78);
}

.overlayButton:hover {
  background-color: #b9b713;
}

.overlayButton:active {
  background-color: #b9b713;
  box-shadow: 0 5px #666;
  transform: translateY(4px);
}
.empty {
  width: 360px;
  height: 260px;
}
.demos {
  text-align: center;
}
.text {
  font-weight: bolder;
  color: rgb(255, 255, 255);
  font-size: 20px;
  width: 50%;
  margin: 10% auto 5%;
}
.overlay {
  cursor: default;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  height: 300px;
  width: 400px;
  opacity: 0;
  transition: 0.5s ease;
  background-color: #008bba;
  border-radius: 10px;
  margin: 0 auto;
}
.cont .overlay:hover {
  opacity: 0.8;
}
.container {
  max-width: 1400px;
}
.logo {
  text-align: center;
  font-weight: bold;
  text-decoration: underline;
}
img {
  border-radius: 10px;
  padding: 0px;
}
</style>
