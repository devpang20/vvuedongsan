<template>
  <div class="black-bg" v-if="isOpen == true">
    <div class="white-bg">
      <img :src="oneRooms[clickIndex].image" style="width:100%">
      <h4>{{ oneRooms[clickIndex].title }}</h4>
      <p>{{ oneRooms[clickIndex].content }}</p>
      <!--      <input @input="month = $event.target.value">-->
      <!-- 축약-->
      <input v-model.number="month">
      <p>{{ month }} 개월 선택함 : {{ oneRooms[clickIndex].price * month }} 원</p>
      <button @click="isOpen = false">닫기</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Modal',
  data() {
    return {
      month : 1
    }
  },
  props : {
    oneRooms : Array,
    clickIndex: Number,
    isOpen: Boolean
  }
}
</script>
<style>
</style>
