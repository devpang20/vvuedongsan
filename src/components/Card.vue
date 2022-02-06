<template>
  <div>
    <img :src="room.image" alt="썸넬" class="room-img">
    <h4 @click="$emit('openModal', room.id)">{{ room.title }} 원룸</h4>
    <p>{{ room.price }} 원</p>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    room: Object,
  },
  methods: {
    send() {
      this.$emit('openModal', this.room.id)
    }

  }
}
</script>
<style>
</style>
