<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <app-bar title="TODO"  left="bars" right="search" />
  </div>
</template>

<script>
// @ is an alias to /src
import AppBar from '../components/appBar.vue'

export default {
  components: {
    AppBar
  }
}
</script>

<style lang="scss">
.home {
  height: 100%;
  width: 100%;
  overflow: hidden;
  color: white;
  text-align: center;
}
</style>
