<template>
<!-- Allen's buttons-->
<div class="topbuttons">
  <button id="Duplicate">New duplicate</button>
  <button id="Color">Toggle color</button>
  <button id="Header">Change heading</button>
  <button id="Delete">Delete 1 card</button>
</div>
<!-- Allen's Card-->
  <div id="card1" class="card">
  <p id="header1" class="header">Team Fortress 2 Pyroland<p>
  <p id="bod1" class="bod">This is a screenshot from a 3D rendered animation posted to Youtube by Valve Corporation to promote the video-game Team Fortress 2</p>
  <p id="bod2" class="bod">The video is called "Meet the Pyro"</p>
  <img class="img" src="https://images.gamebanana.com/img/ss/mods/54f8f277e231a.webp" alt="">
  <button id="Details" class="button">Details</button>
  </div>
<!-- End of Allen's cards-->
</template>

<script setup>
import { defineProps, reactive } from 'vue'

defineProps({
  msg: String
})

const state = reactive({ count: 0 })
</script>

<style scoped>
a {
  color: #42b983;
}

.alt {
  width: 500px;
  height: 565px;
  border: 14px solid #72fc79;
  background-color: cyan;
  text-align: center;
  border-radius: 20px;
}
.topbuttons {
  display: block;
}

button {
  font-size: 24px;
  margin-top: 12px;
  margin-bottom: 12px;
  background-color: #94FEFB;
  font-family: "Monaco", Monospace;
  border: 4px solid pink;
  border-radius: 20px;
}

/*BELOW IS ALL ORIGINAL CARD SPACE*/

.card {
  width: 500px;
  height: 565px;
  border: 14px solid pink;
  background-color: #FB94FE;
  text-align: center;
  border-radius: 20px;
}

.header {
  color: #94FEFB;
  font-family: "Lucida Console", monospace;
  font-size: 30px;
  border: 2px solid;
  border-radius: 16px;
  Margin: 16px;
  padding: 8px;
  background-color: #ff66cc;
}

.bod {
  color: blue;
  font-family: "Monaco", Monospace;
  font-size: 20px;
  margin-left: 8px;
  margin-right: 8px;
  visibility: hidden;
}

.img {
  width: 460px;
  height: 250px;
  border: 2px inset #94FEFB;
  padding: 8px;
  background-color: #ff66cc;
  border-radius: 20px;
}

.button {
  background-color: hotpink;
  color: #94FEFB;
  padding: 8px;
  border: 2px dashed #94FEFB;
  font-family: "Monaco", Monospace;
  visibility: hidden;
  border-radius: 24px;
  margin-top: 0px;
  font-size: 20px;
}

.topbuttons button:hover,
.topbuttons button:focus {
  color: hotpink;
  background-color: #94FEFB;
}

.topbuttons button:active {
  color: #94FEFB;
  background-color: #ec72fc
}

@media screen and (max-width: 800px) and (min-width: 500px) {
  .button {
    visibility: visible;
  }
}

@media screen and (max-width: 500px) {
  .card {
    width: auto;
    height: auto;
  }
  .img {
    width: 90%;
    height: auto;
  }
  .header{
    font-size: 4vw;
  }
  .bod {
    font-size: 4vw;
  }
}
</style>