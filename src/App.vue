<template>
  <div id="app">
    <!--<img src="./assets/logo.png">-->
    <Pyheader></Pyheader>
    <top></top>
    <index></index>
    <!--<router-view/>-->

  </div>
</template>

<script>
  import Pyheader from 'components/header'
  import top from 'components/top'
  import index from 'components/index'
export default {
  name: 'App',
  components:{
    top,
    Pyheader,
    index
  }
}
</script>

<style>
#app {
}
</style>
