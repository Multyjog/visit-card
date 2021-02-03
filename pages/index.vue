<template>
  <div>
    <div class="container mb-5">
      <div class="commerce">BEST MATCH FOR YOU</div>
      <div class="row">
        <div class="col-md-3 cont">
          <img class="photo" src="../static/me.jpeg" alt="" />
          <div class="overlay" @click="toggleClicked()">
            <div class="text">No hidden content here</div>
          </div>
          <h3 class="me">Thats me</h3>
        </div>
        <div style="float:none" class="col-md-1"></div>
        <div class="col-md-8">
          <h1 class="myTitle mb-5">Little about me</h1>
          <label
            >I live in Moscow. Love extremely sports like: Snowboard and
            Longboard. I drive a bike, and also kind of funny and interesting
            person. Contact me, you will like it!
          </label>
          <form>
            <div>
              <label>
                I still don't have a good CV. So please, help me complete it.
                Just <span>hit</span> any buttons on your keyboard and my good
                friend JavaScript will do all work for you! :-)
              </label>
              <Typer :text="text" />
              <div class="mybtn mt-3">
                <button class="butt" title="Actually dont need to ;)">
                  Send this one to me
                </button>
              </div>
            </div>
          </form>
          <SocialButtons />
        </div>
      </div>
      <div :class="{ 'hidden-content': true, hidden: !isClicked }">
        <div class="meeter mt-5">
          <h1>Oh okay, you got me!</h1>
          <h4>Take this video as easter egg</h4>
          <iframe
            width="80%"
            height="450px"
            src="https://www.youtube.com/embed/7yLxxyzGiko"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
          ></iframe>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
const text = `Hello, my name is Simon. I am from Moscow. Right now, I improve my skills in web development and more specifically in Vue.js. 
There are some skills that could be useful for your project: 
- I always seek to learn new things and try to find information I need by myself
- I can handle time management, and always available during working ours  
- I have experience with project management tools like Jira/Trello, and always update my progress and status
- I use version control system and follow 'Keep a Changelog'

Regards, Simon`;
export default {
  data() {
    return { isClicked: false, text: text };
  },
  methods: {
    toggleClicked() {
      if (this.isClicked) return;
      this.isClicked = true;
      let hidden = this.$el.querySelector(".hidden-content");
      setTimeout(() => {
        hidden.scrollIntoView();
      }, 0);
    }
  }
};
</script>

<style scoped>
.container {
  max-width: 1400px;
}
.butt {
  background-color: green;
  color: white;
  font-weight: bold;
}
.hidden {
  display: none !important;
}
.meeter {
  text-align: center;
}
.myTitle {
  text-align: center;
  font-weight: bold;
}
label {
  font-weight: bolder;
  font-size: larger;
}
button {
  border-radius: 15px;
  border-style: none;
}
.mybtn {
  text-align: center;
}
span {
  font-weight: bolder;
}
.overlay {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  height: auto;
  width: 100%;
  opacity: 0;
  transition: 0.5s ease;
  background-color: #008bba86;
  border-radius: 10px;
}
.commerce {
  text-align: center;
  font-size: 4rem;
  font-weight: bolder;
  color: rgba(255, 255, 255, 0.849);
  text-shadow: 4px 3px rgb(36, 36, 36);
  margin: 1rem auto 2rem;
}
.cont:hover .overlay {
  opacity: 0.5;
}
.cont {
  padding: 0px !important;
  margin: auto 0 auto 0;
}
.text {
  cursor: pointer;
  text-align: center;
  font-weight: bolder;
  color: rgb(255, 255, 255);
  font-size: 20px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
}
.photo {
  max-width: 100%;
  height: auto;
  width: auto;
  border-radius: 10px 10px 0px 0px;
}
.me {
  text-align: center;
  background-color: aliceblue;
  width: 100%;
  border-radius: 0px 0px 10px 10px;
  margin: 0;
}
</style>
