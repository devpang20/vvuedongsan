<template>
  <div id="app">
    <div class="menu">
      <a>Home</a>
      <a>Products</a>
      <a>About</a>
    </div>
    <img alt="Vue logo" src="./assets/logo.png">
    <div v-for="(product, i) in products" :key="i">
      <h4>{{ product }} 원룸</h4>
      <p>가격은 아무거나~</p>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      products: ['역삼동원룸', '천호동원룸', '마포구원룸']
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
</style>
