<template>
  <div id="app">
    <div class="black-bg" v-if="isOpen == true">
      <div class="white-bg">
        <h4>상세페이지</h4>
        <p>상세페이지 내용임</p>
        <button @click="isOpen = false">닫기</button>
      </div>
    </div>
    <div class="menu">
      <a v-for="(a, i) in menus" :key="i" >{{ a }}</a>
    </div>
    <img alt="Vue logo" src="./assets/logo.png">
    <div>
      <img src="./assets/room0.jpg" alt="썸넬" class="room-img">
      <h4 @click="isOpen = true">{{ products[0] }} 원룸</h4>
      <p>가격은 아무거나~</p>
      <button @click="count[0]++">허위매물</button> <span>신고수 : {{ count[0] }}</span>
    </div>
    <div>
      <img src="./assets/room1.jpg" alt="썸넬" class="room-img">
      <h4 @click="isOpen = true">{{ products[1] }} 원룸</h4>
      <p>가격은 아무거나~</p>
      <button @click="count[1]++">허위매물</button> <span>신고수 : {{ count[1] }}</span>
    </div>
    <div>
      <img src="./assets/room2.jpg" alt="썸넬" class="room-img">
      <h4 @click="isOpen = true">{{ products[2] }} 원룸</h4>
      <p>가격은 아무거나~</p>
      <button @click="count[2]++">허위매물</button> <span>신고수 : {{ count[2] }}</span>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  //react 의 state
  data() {
    return {
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
