<template>
    <div>
      <bannerbox></bannerbox>
      <newMessage></newMessage>
    </div>
</template>

<script>
  import bannerbox from './bannerbox'
  import newMessage from './newMessage'
    export default {
        name: "index",
        components:{
            bannerbox,
            newMessage
        }
    }
</script>

<style scoped>

</style>
