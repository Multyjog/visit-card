<template>
  <div>
    <div class="container mb-5">
      <div class="commerce">BEST MATCH FOR YOU</div>
      <div class="row">
        <div class="col-md-3 cont">
          <img class="photo" src="~assets/me.jpeg" alt="" />
          <div class="overlay" @click="toggleClicked()">
            <div class="text">No hidden content here</div>
          </div>
          <h3 class="me">
            Person of the Year 2006.
            <h3 class="little">According to <span>"Time"</span> magazine</h3>
          </h3>
        </div>
        <div style="float:none" class="col-md-1"></div>
        <div class="col-md-8">
          <h1 class="myTitle mb-5">Little about me</h1>
          <label class="mb-4"
            ><span>Hello,</span>
            <p>
              I am Simon, a Frontend Developer. I am from Moscow, but now I live
              in a coworking space in Antalya, in a company of developers that
              have 5+ and 10+ years of Full Stack experience. I learn something
              new from them every day, what I could not learn by myself without
              experience in development:
            </p>
            <ul>
              <li>Create reusable yet simple components and functions</li>
              <li>Use modern JavaScript techniques and tools</li>
              <li>
                Follow "Keep a Changelog", and manage Git branches and commits
                correctly
              </li>
              <li>Estimate and prioritize tasks</li>
              <li>Follow best practices and respect deadlines</li>
            </ul>
            <p>
              I have some experience with SPA techologies. I know how to set up
              REST API server and client. Every day I work and improve my Vue.js
              skills, and also use Nuxt.js for SSR applications. I use
              responsive design guidelines in my projects. I like to add a
              little bit of humor.
            </p>
            <p>
              Please,contact me if you have a position for me in your project or
              need an additional info!
            </p>
            <p>Regards, Simon</p>
          </label>
          <!-- <form>
            <div>
              <Typer :text="text" />
              <div class="mybtn mt-3">
                <a
                  class="btn-grad"
                  type="button"
                  title="Actually dont need to ;)"
                >
                  Send this one to me
                </a>
              </div>
            </div>
          </form> -->
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
export default {
  data() {
    return { isClicked: false };
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
.tooltip {
  position: relative;
  display: inline-block;
  border-bottom: 1px dotted black;
}

.tooltip .tooltiptext {
  visibility: hidden;
  width: 120px;
  background-color: black;
  color: #fff;
  text-align: center;
  border-radius: 6px;
  padding: 5px 0;
  position: absolute;
  z-index: 1;
  bottom: 150%;
  left: 50%;
  margin-left: -60px;
}

.tooltip .tooltiptext::after {
  content: "";
  position: absolute;
  top: 100%;
  left: 50%;
  margin-left: -5px;
  border-width: 5px;
  border-style: solid;
  border-color: black transparent transparent transparent;
}

.tooltip:hover .tooltiptext {
  visibility: visible;
}
.container {
  max-width: 1400px;
}
.btn-grad {
  background-image: linear-gradient(
    to right,
    #215f00 0%,
    #0f2c06 51%,
    #215f00 100%
  );
  border-radius: 10px;
  text-transform: uppercase;
  transition: 0.8s;
  background-size: 200% auto;
  color: white;
  font-size: 1rem;
  font-weight: bold;
  padding: 0.5rem 0.8rem;
}
.btn-grad:hover {
  background-position: right center; /* change the direction of the change here */
  color: rgb(255, 255, 255);
  text-decoration: none;
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
  text-decoration: underline;
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
  font-size: 110%;
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
  padding: 5px 0px 1px 0;
  font-size: 15px;
  background-color: white;
  text-align: center;
  width: 100%;
  border-radius: 0px 0px 10px 10px;
  margin: 0;
}
.little {
  font-size: 15px;
}
</style>
