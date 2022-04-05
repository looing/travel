<template>
  <div class="header">
      <div class="header-left">
          <span class="iconfont back-icon">&#xe624;</span>
      </div>
      <div class="header-input">
          <span class="iconfont">&#xe632;</span>
          输入城市\游玩\主题\景区
      </div>
      <div class="header-right">
          城市
          <span class="iconfont down-icon">&#xe64a;</span>
      </div>
  </div>
</template>

<script>
export default {
    name: "HomeHeader"
}
</script>

<style lang="stylus" scoped>
    @import '~css/variables';
    .header
        display: flex
        height: .86rem
        background-color: $bgColor
        color: #fff
        .header-left
            width: .84rem
            line-height: .86rem
            float: left
            text-align: center
            .back-icon
                font-size: .4rem
        .header-input
            flex: 1
            margin-top: .1rem
            margin-left: .1rem
            height: .64rem
            color: #ccc
            line-height: .64rem
            background-color: #fff
            border-radius: 0.1rem
            padding-left: .2rem
        .header-right
            width: 1.24rem
            float: right
            text-align: center
            line-height: .86rem
            margin-left: -.04rem
            .down-icon
                font-size: .2rem

</style>