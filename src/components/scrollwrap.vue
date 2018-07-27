<template>
  <div class="scroll-wrap">
    <ul class="scroll-content" :style="{ top }">

      <li v-for="item in prizeList">
        <transition name="slide-trans">
          <a href="{item.linkurl}">{{item.message}}</a>
        </transition>
      </li >
    </ul>
  </div>
</template>

<script>
    export default {
        name: "scrollwrap",
        props: {
          prizeList: {
            type: Array,
            default: []
          },
          inv: {
            type: Number,
            default: 2000
          }
        },
        data () {
          return {
            activeIndex: 0
          }
      },

      computed: {
        top() {
          return - this.activeIndex * 50 + 'px';
        }
      },

      mounted() {
        setInterval(_ => {
          if(this.activeIndex < this.prizeList.length) {
            this.activeIndex += 1;
          } else {
            this.activeIndex = 0;
          }
        }, this.invs);
      }
    }
</script>

<style scoped>
  .slide-trans-enter-active {
    transition: all .5s;
  }
  .slide-trans-enter {
    transform: translateY(200px);
  }
  .slide-trans-old-leave-active {
    transition: all .5s;
    transform: translateY(-200px);
  }

  .scroll-wrap{
    width: 200px;
    height: 50px;
    border: 1px solid blue;
    overflow: hidden;
  }

  .scroll-content{
    position: relative;
    transition: top 0.5s;
  }

  .scroll-content li{
    line-height: 50px;
    text-align: center;
  }

</style>
