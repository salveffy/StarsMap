<template>
  <div class="contain-btn">
    <iframe
      width="100%"
      height="100%"
      frameborder="0"
      scrolling="no"
      marginheight="0"
      marginwidth="0"
      src="https://virtualsky.lco.global/embed/index.html?longitude=60.00812450775173&latitude=30.394269753389032&gradient=false&projection=stereo&constellations=true&scalestars=2&magnitude=10&az=20&clock=Fri%20Aug%2030%202019%2018:00:00%20GMT+0300%20(%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D0%B0,%20%D1%81%D1%82%D0%B0%D0%BD%D0%B4%D0%B0%D1%80%D1%82%D0%BD%D0%BE%D0%B5%20%D0%B2%D1%80%D0%B5%D0%BC%D1%8F)"
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
