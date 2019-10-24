<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <app-bar title="TODO"  left="bars" right="search" />
    <avatar />
  </div>
</template>

<script>
// @ is an alias to /src
import AppBar from '../components/AppBar.vue'
import Avatar from '../components/Avatar.vue'

export default {
  components: {
    AppBar,
    Avatar
  }
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
