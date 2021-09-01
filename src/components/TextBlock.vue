<template>
  <div>
    <div class="title">Звездное небо - это круто !</div>
    <div class="text">
      Так почему бы не посмотреть на него более детально ?</div>
  </div>
</template>

<script>
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
  name:'TextBlock',
})
</script>

<style scoped>
.title {
  padding: 15px;
  color: white;
  font-size:42px;
}
.text {
  color:white;
  font-size:25px;
}
 @media screen and (max-width: 700px) {
.title {
  padding: 15px;
  color: white;
  font-size:25px;
}
.text {
  color:white;
  font-size:17px;
}

 }
</style>