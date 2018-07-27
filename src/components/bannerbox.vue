<template>
  <div class="bannerbox">
    <carousel :slides="slides" :inv="invTime"></carousel>
  </div>
</template>

<script>
  import carousel from './Carousel'
  export default {
        name: "index",
        data () {
          return {
            invTime: 3000,
            slides: [
              {
                src:require('../../static/img/banner.jpg'),
                title:'xxx1',
              },
              {
                src:require('../../static/img/aboutUs.jpg'),
                title:'xxx2'
              },
              {
                src:require('../../static/img/connection.png'),
                title:'xxx3'
              }
            ]
          }
      },
      components: {
        carousel
      }
    }
</script>

<style scoped>
  .bannerbox {
    position: relative;
    width: 100%;
    height: 360px;
    overflow: hidden;
    min-width: 1200px;
  }


</style>
