<template>
    <div class="notice">
      <div class="row">
        <div class="hd">
            <span class="start"></span>
            <span>最新消息</span>
            <em class="icon-notice"></em>
        </div>

        <scrollwrap1 :prizeList="prizeList" :inv="invTime"></scrollwrap1>

      </div>
    </div>
</template>

<script>
    import scrollwrap1 from './scrollwrap'
    export default {
        name: "newMessage",
        data(){
          return{
            prizeList: [
              { message: 0 ,linkurl:"https://www.baidu.com"},
              { message: 1,linkurl:"https://www.baidu.com" },
              { message: 2 ,linkurl:"https://www.baidu.com"},
              { message: 3,linkurl:"https://www.baidu.com" },
              { message: 4,linkurl:"https://www.baidu.com" }
            ],
            invTime:10000
          }
        },
      components:{
        scrollwrap1,
      }
    }
</script>

<style scoped>
  .notice{
    border-bottom: 1px solid #0c4cc8;
    height: 60px;
    line-height: 20px;
  }

  .notice .hd{
    width: 160px;

  }
  .notice .hd span{
    padding-left: 35px;
    font-size:14px;
    font-family:"Microsoft YaHei UI";
    color: #0595dc;
  }

  .notice .hd .start{
    display: inline-block;
    height: 43px;
    width: 5px;
    background-color: #0595dc;
    padding: 0;
    margin-bottom: -14px;
    margin-right: 22px;
  }

  .scrollwrap{
    display: block;
    width: 100px;
    height: 60px;
    line-height: 20px;
  }

  .row{
    margin: 0 auto;
    width: 1200px;
    height: 60px;
    position: relative;
  }
</style>
