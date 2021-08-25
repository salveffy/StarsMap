<template>
  <div id="app">
    <div class="container-app" v-if="isVisiable">
      <div class="logo-cont">
        <img class="logo" src="./assets/logo.png" width="600px" height="600px">
        <img class="logo-circ" src="./assets/logo-circ.png" width="600px" height="600px">
      </div>
          <div class="contain">
            <TextBlock></TextBlock>
            <button class="button" @click="isVisiable = !isVisiable">Звездное небо</button>
          </div>
    </div>
    <SkyMap v-else msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import SkyMap from './components/SkyMap.vue'
import TextBlock from './components/TextBlock.vue'

export default {
  name: 'App',
  components: {
    SkyMap,
    TextBlock
  },
  data:() => ({
    isVisiable: true,
  })
}
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  text-align: center;
}
body {
  margin:0;
  padding: 0;
  background-color: black;
}
.container-app{
  width:100vw;
  height: 100vh;
  display:flex;
  justify-content: space-around;
  align-items: center;
}
.logo-circ{
  position: absolute;
  left:3.9%;
  top:18.7%;
  animation: 0.1s linear 0s normal none infinite running rot;
  -webkit-animation: 30s linear 0s normal none infinite running rot;
}
@keyframes rot {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
@-webkit-keyframes rot {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
.button {
  background-color: rgba(0, 0, 0, 0.836);
  color: rgb(255, 255, 255);
  border: 2px solid #ffffff;
  padding: 16px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  -webkit-transition-duration: 0.4s; /* Safari */
  transition-duration: 0.4s;
  cursor: pointer;
  border-radius: 30px;
  margin-top:30px;
}
.button:hover {
  background-color: #ffffff;
  color: rgb(0, 0, 0);
}

  @media screen and (max-width: 450px) {
.container-app{
  width:100vw;
  height: 100vh;
  display:flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
}
.logo-cont{
  width:270px;
  height:270px;
}
.logo {
  width:270px;
  height: 270px;
}
.logo-circ {
  width:270px;
  height: 270px;
  left:13.9%;
  top:9.3%;
}
  }
</style>
