<template>
  <div>
    <div class="container mb-5">
      <div class="commerce">BEST MATCH FOR YOU:</div>
      <div class="row">
        <div class="col-md-4 cont">
          <img class="photo" src="../static/me1.jpeg" alt="">
          <div class="overlay">
            <div class="text">Contacts</div>
          </div>
          <h3 class="me">Thats me</h3>
        </div>
        <div class="col-md-8">
          <h2>Little about me</h2>
          <p>I live in Moscow. Love extremely sports like: Snowboard and Longboard.
            I drive a bike, and also kind of funny and interesting person. Contact me, you will like it!
          </p>
          <form>
            <div>
              <label>
                I still don't have a good CV. So please, help me complete it.</label>
                Just <span>hit</span> any buttons on your keyboard and my good friend JavaScript will do all work for you! :-) 
              <textarea @keydown.prevent="increaseCounter()" @keydown.backspace.prevent="decreaseCounter()" :value="showContent" 
              class="form-control" id="formText" rows="3"></textarea>
              <div class="mybtn mt-3">
                <button title="Actually dont need to ;)" >Send this one to me</button>
              </div>
            </div>
          </form> 
          <div class="social-buttons row mt-5">  <!-- Gonna show by press the overlay -->
            <h1 class="col-md-3"><a href="https://www.instagram.com/multyjog/?hl=ru" title="My Instagram" target="_blank"><font-awesome-icon :icon="['fab','instagram']"/></a></h1>
            <h1 class="col-md-3"><a href="https://www.facebook.com/semen.kotov.315/" title="My FaceBook" target="_blank"><font-awesome-icon :icon="['fab','facebook-f']"/></a></h1>
            <h1 class="col-md-3"><a href="https://stackoverflow.com/users/15061974/%d0%a1%d0%b5%d0%bc%d1%91%d0%bd-%d0%9a%d0%be%d1%82%d0%be%d0%b2" title="My StackOverflow" target="_blank"><font-awesome-icon :icon="['fab','stack-overflow']"/></a></h1>
            <h1 class="col-md-3"><a href="https://github.com/Multyjog" title="My GitHub" target="_blank"><font-awesome-icon :icon="['fab','github']"/></a></h1>

          </div>
        </div>
      </div>
    </div>
  </div>  
</template>

<script>
const formContent = `Hello, my name is Simon. I am from Moscow. Right now, I improve my skills in web development and more specifically in Vue.js. 
There are some skills that could be useful for your project: 
- I always seek to learn new things and try to find information I need by myself
- I can handle time management, and always available during working ours  
- I have experience with project management tools like Jira/Trello, and always update my progress and status
- I use version control system and follow 'Keep a Changelog'

Regards, Simon`
export default {
data() {
return {counter:0}
},
methods:{
 increaseCounter() {
   this.counter = Math.min(this.counter +3, formContent.length )
 },
 decreaseCounter() {
   this.counter = Math.max(this.counter -6, 0);
 }
},
computed:{
  showContent() {
    return formContent.substring(0,this.counter)
  }
},
}
</script>

<style scoped>
#formText {
  height: 260px;
}
.social-buttons {
  text-align: center;
}
a {
  text-decoration: none;
  color: white;
}
button {
  border-radius: 15px;
  border-style: none;
}
.mybtn {
  text-align: center;
}
body {
  font-family: sans-serif;
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
  height: 100%;
  width: 100%;
  opacity: 0;
  transition: .5s ease;
  background-color: #008CBA;
  border-radius: 10px;
}
.commerce {
  text-align: center;
  font-size: 4rem;
  font-weight: bolder;
  color: rgba(255, 255, 255, 0.849);
  text-shadow: 4px 3px rgb(36, 36, 36)
}
.cont:hover .overlay {
  opacity: 0.5;
}
.cont {
  padding: 0px !important;
}
.text {
  color: white;
  font-size: 20px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
}
.photo{
  max-width: 100%;
  height: auto;
  width: 100%;
  border-radius: 10px 10px 0px 0px;
}
.me {
  text-align: center;
  background-color: aliceblue;
  width: 100%;
  border-radius: 0px 0px 10px 10px;

}


</style>
