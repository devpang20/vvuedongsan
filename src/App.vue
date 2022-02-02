<template>
  <div id="app">
    <Modal :oneRooms="oneRooms" :clickIndex="clickIndex" :isOpen="isOpen" />
    <div class="menu">
      <a v-for="(a, i) in menus" :key="i" >{{ a }}</a>
    </div>
    <Discount/>
    <div v-for="(room, i) in oneRooms" :key="i">
      <img :src="room.image" alt="썸넬" class="room-img">
      <h4 @click="isOpen = true; clickIndex = i">{{ room.title }} 원룸</h4>
      <p>{{ room.price }}</p>
    </div>
  </div>
</template>

<script>

import data from './assets/oneroom'
import Discount from './components/Discount'
import Modal from './components/Modal'

export default {
  name: 'App',
  //react 의 state
  data() {
    return {
      oneRooms :data,
      clickIndex : 0,
      isOpen: false,
      count: [0, 0, 0],
      menus: ['Home', 'Shop', 'About'],
      products: ['역삼동원룸', '천호동원룸', '마포구원룸']
    }
  },
  methods : {
    increase(i) {
      this.count[i]++
    }
  },
  components: {
    Discount,
    Modal
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.menu {
  background : darkslateblue;
  padding : 15px;
  border-radius : 5px;
}
.menu a {
  color : white;
  padding : 10px;
}
.room-img {
  width: 100%;
  margin-top: 40px;
}
body {
  margin : 0;
}
div {
  box-sizing: border-box;
}
.black-bg {
  width: 100%; height:100%;
  background: rgba(0,0,0,0.5);
  position: fixed; padding: 20px;
}
.white-bg {
  width: 100%; background: white;
  border-radius: 8px;
  padding: 20px;
}
</style>
