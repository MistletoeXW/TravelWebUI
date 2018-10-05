<template>
  <div class="icons">
    <div class="icon">
      <div class="icon-img">
        <img class="icon-img-1" src="../../../assets/img/food.png"/>
        <p class="icon-content">美食</p>
      </div>
    </div>
    <div class="icon">
      <div class="icon-img">
        <img class="icon-img-1" src="../../../assets/img/moive.png"/>
        <p class="icon-content">电影</p>
      </div>
    </div>
      <div class="icon">
        <div class="icon-img">
          <img class="icon-img-1" src="../../../assets/img/play.png"/>
          <p class="icon-content">休闲娱乐</p>
        </div>
      </div>
      <div class="icon">
        <div class="icon-img">
          <img class="icon-img-1" src="../../../assets/img/woman.png"/>
          <p class="icon-content">化妆品</p>
        </div>
      </div>
      <div class="icon">
        <div class="icon-img">
          <img class="icon-img-1" src="../../../assets/img/buy.png"/>
          <p class="icon-content">购物</p>
        </div>
      </div>
      <div class="icon">
        <div class="icon-img">
          <img class="icon-img-1" src="../../../assets/img/waimai.png"/>
          <p class="icon-content">外卖</p>
        </div>
      </div>
      <div class="icon">
        <div class="icon-img">
          <img class="icon-img-1" src="../../../assets/img/hotel.png"/>
          <p class="icon-content">酒店</p>
        </div>
      </div>
      <div class="icon">
        <div class="icon-img">
          <img class="icon-img-1" src="../../../assets/img/run.png"/>
          <p class="icon-content">运动健身</p>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'HoemIcons'
}
</script>

<style lang="stylus" scoped>
  .icons
    overflow : hidden
    height : 0
    padding-bottom :  50%          //高度占比50%，宽度占比100%
  .icon
    position :relative
    overflow : hidden
    float: left
    width : 25%
    height :0
    padding-bottom : 25%      //高度占比25%，宽度占比25%
    .icon-img
      position : absolute
      top: 0
      left: 0
      right: 0
      bottom : 4%
      box-sizing: border-box
      padding: 17%            //图片下预留空隙
      .icon-img-1
        display: block
        margin: 0 auto
        height:100%
    .icon-content
      position: absolute
      left: 0
      right: 0
      bottom: 0
      height: 4%
      line-height: 4%
      text-align : center

</style>
