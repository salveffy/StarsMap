<template>
  <div class="contain-btn">
    <iframe
      width="100%"
      height="100%"
      frameborder="0"
      scrolling="no"
      marginheight="0"
      marginwidth="0"
      src="https://virtualsky.lco.global/embed/index.html?longitude=-119.86286000000001&latitude=34.4326&gradient=false&projection=stereo&cardinalpoints=false&constellations=true&showplanets=false&magnitude=10&live=true&az=117.5"
      allowTransparency="true"
    ></iframe>
  </div>
</template>

<script>
export default {
  name: 'SkyMap',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
body {
  margin: 0;
  padding: 0;
}
.contain-btn {
  width: 100vw;
  height: 100vh;
}
</style>
