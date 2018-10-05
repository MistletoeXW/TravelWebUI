<template>
  <div>
    <div class="recommend-title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="(item,index) of recommendList" :key="index">
        <img class="item-img" :src="item.imgUrl"/>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    recommendList: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '../../../assets/style/mixins.styl' //字数 超过显示框自动转化为 "……"
  .recommend-title
    margin-top : 20px
    line-height : 40px
    background : #cccbc9
    text-indent: 5px
  .item
    overflow : hidden
    display : flex
    height : 105px
    .item-img
      width: 90px
      height: 90px
      padding : 5px  //上下左右间距
    .item-info
      flex: 1
      min-width : 0
      .item-title
        line-height: 36px
        font-size: 20px
        padding : 0 5px
        ellipsis()
      .item-desc
        line-height : 20px
        padding : 0 5px
        color : #403f3f
        ellipsis()
      .item-button
        background : #0799f4
        padding : 0 5px
        border-radius : 6px
        margin-top : 15px
        color : aliceblue
 </style>
