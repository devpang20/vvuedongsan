<template>
  <div>
    <img :src="room.image" alt="썸넬" class="room-img">
    <h4>{{ room.title }} 원룸</h4>
    <p>{{ room.price }} 원</p>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    room: Object,
  }
}
</script>
<style>
</style>
