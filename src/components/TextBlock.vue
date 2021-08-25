<template>
  <div>
    <div class="title">Наша первая встреча прошла под этими звездами</div>
    <div class="text">Звездное небо - это круто !<br>
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
 @media screen and (max-width: 450px) {
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