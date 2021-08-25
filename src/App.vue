<template>
  <div id="app">
    <div class="container-app" v-if="isVisiable">
      <div>
        <img src="./assets/jopa.png" alt="jopa" width="30%" height="30%">
      </div>
      <div class="logo-cont">
        <img class="logo" src="./assets/logo.png" width="40%" height="40%">
        <img class="logo-circ" src="./assets/logo-circ.png" width="40%" height="40%">
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

.contain {
  padding-right: 310px;
  width:100%;
  z-index:5;
}

.logo {
  position: relative;
  left:20%;
}
.logo-cont {
  margin:0;
  position:absolute;
  width:80%;
  left:-15%;
}
.logo-circ{

  position: relative;
  left:-20%;
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

  @media screen and (max-width: 700px) {
.container-app{
  width:100vw;
  height: 100vh;
  display:flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
}

.logo {
  margin-top:-60%;
  width:60%;
  position: relative;
  left:30%;
}
.logo-cont {
  margin:0;
  position:absolute;
  width:80%;
  left:-15%;


}
.logo-circ{
  width:60%;
  position: relative;
  padding-top:-80%;
  margin-top:-80%;
  left:30%;
  margin-bottom:5.2%;
}

.contain{
  padding-right: 0;
}

  }
</style>
