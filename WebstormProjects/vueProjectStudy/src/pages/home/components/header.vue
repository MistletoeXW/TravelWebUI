<template>
   <div class="header">
     <div class="header-left">
       <div class="iconfont back-icon">&#xe624;</div>
     </div>
     <div class="header-input">
       <span class="iconfont">&#xe632;</span>
       输入城市、景点、主题
     </div>
     <div class="header-right">
       城市
       <span class="iconfont">&#xe62d;</span>
     </div>
   </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  .header
    display:flex
    line-height: 50px
    background #0a87ff
    color: #fff
    .header-left
      width: 36px
      float: left
      .back-icon               //返回图标的大小和位置
        text-align: center
        font-size: 24px
    .header-input
      flex:1
      height: 36px
      line-height: 36px
      margin-top: 6px
      margin-left: 8px
      padding-left: 15px   //搜索图标离搜索框左侧的距离
      background :#fff
      border-radius:5px     //搜索框的圆角
      color:#ccc
    .header-right
      width: 64px
      float: right
      text-align: center
</style>
