<template>
<!-- Allen's buttons-->
<button id="Duplicate" class="DuplicateBut">New duplicate</button>
<button id="Toggle" class="ToggleButt">Toggle color</button>
<button id="Header" class="HeaderButt" type="button">Change heading</button>
<button id="Delete" class="DeleteButt">Delete 1 card</button>
<button id="Details" class="DetailsButt">Details</button>
<!-- Allen's Card-->
  <div id="card1" class="card">
  <p id="header1" class="header">Team Fortress 2 Pyroland<p>
  <p id="bod1" class="bod">This is a screenshot from a 3D rendered animation posted to Youtube by Valve Corporation to promote the video-game Team Fortress 2</p>
  <p id="bod2" class="bod">The video is called "Meet the Pyro"</p>
  <img class="img" src="https://images.gamebanana.com/img/ss/mods/54f8f277e231a.webp" alt="">
  <a class="button" id="details" onclick="myFunc()">Details</a>
    <script> 
      function myFunc() {
  if (document.getElementById('bod1').style.visibility == 'hidden') 
  {document.getElementById('bod1').style.visibility = 'visible'; document.getElementById('bod2').style.visibility = 'visible'; }
  else
    {document.getElementById('bod1').style.visibility = 'hidden'; document.getElementById('bod2').style.visibility = 'hidden'; }
      }
    </script>
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
.DuplicateBut {
  font-size: 50px;
  display: block;
  background-color: red;
}
.ToggleButt {
  font-size: 50px;
  display: block;
  background-color: green;
}
.HeaderButt {
  font-size: 50px;
  display: block;
  background-color: yellow;
}
.DeleteButt {
  font-size: 50px;
  display: block;
  background-color: skyblue;
}
.DetailsButt {
  font-size: 50px;
  display: block;
  background-color: orange;
}
.alt {
  width: 500px;
  height: 565px;
  border: 14px solid pink;
  background-color: magenta;
  text-align: center;
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
  margin-bottom: 12px;
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
  margin: 80px;
}

.button:hover {
  color: hotpink;
  background-color: #94FEFB;
}

button:focus {
  color: #03fc0b;
  background-color: #ff0037;
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
</style>
