<template>
    <div class="control">
      <div class="container">
        <div class="logbox">
          <h2 class="left logo">
            <a href="/">
              <img src="/static/img/logo.jpg" width="53" height="53">
            </a>
          </h2>
          <p class="right searchbox">
            <input type="text" class="left lw keyword" name = "keyword" />
            <input type="button" class="left search"/>
          </p>
        </div>
      </div>
      <div class="navebox">
        <ul class="container nave">
          <li>
            <a href="/" class="icon-h">首页</a>
          </li>
          <li class="z">
            <a href="/" class="icon-b">交易大厅</a><span class="hot"></span>
          </li>
          <li class="se">
            <a href="/" class="icon-s">银行快贴</a>
          </li>
          <li>
            <a href="/" class="icon-l">业务合作</a>
          </li>
        </ul>
      </div>
    </div>
</template>

<script>
    export default {
        name: "top"
    }
</script>

<style scoped>
  .container{
    width: 1200px;
    margin: 0 auto;
  }
  .logbox{
    height: 98px;
  }
</style>
