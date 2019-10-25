<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <app-bar title="TODO"  left="bars" right="search" />
    <avatar />
  </div>
</template>

<script>
// @ is an alias to /src
// import AppBar from '../components/AppBar.vue'
// import Avatar from '../components/Avatar.vue'
const path = require('path')
const files = require.context('../components/home',false, /\.vue$/)

// ["./AppBar.vue","./Avatar.vue"]
// console.log("==========:%j",files.keys());  


const modules = {}
files.keys().forEach(key => {
  let name = path.basename(key,'.vue');
  // console.log("name ",name);  // AppBar | Avatar
  
  modules[name] = files(key).default || files(key)
});

// 使用require.context()来减少重复导入的工作量
export default {
  // components: {
  //   AppBar,
  //   Avatar
  // }

  components: modules
}
</script>

<style lang="scss">
.home {
  height: 100%;
  width: 100%;
  overflow: hidden;
  color: white;
  background-color: rgb(17, 241, 241);
}
</style>
