<template>
  <div class="black-bg" v-if="isOpen == true">
    <div class="white-bg">
      <img :src="oneRooms[clickIndex].image" style="width:100%">
      <h4>{{ oneRooms[clickIndex].title }}</h4>
      <p>{{ oneRooms[clickIndex].content }}</p>
      <p>{{ oneRooms[clickIndex].price }} 원</p>
      <button @click="isOpen = false">닫기</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Modal',
  props : {
    oneRooms : Array,
    clickIndex: Number,
    isOpen: Boolean
  }
}
</script>
<style>
</style>
