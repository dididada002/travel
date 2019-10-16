<template>
    <div class="header">
        <div class="header-left">
            <span class="iconfont back-icon">&#xe65c;</span>
        </div>
        <div class="header-input">
            <span class="iconfont">&#xe63c;</span>
            输入城市/景点/游玩主题
        </div>
        <div class="header-right">
            城市
            <span class="iconfont">&#xe643;</span>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="stylus" scoped>
    @import '~styles/varibles.styl'
    .header
        display flex
        line-height: .86rem
        background-color: $bgColor
        color : #fff
        .header-left
            width: .64rem
            float: left
            .back-icon
                text-align center
                font-size .5rem
        .header-right
            width: 1.24rem
            float: right
            text-align: center
        .header-input
            flex: 1
            background-color: #fff
            border-radius: .1rem
            padding-left .2rem
            height .64rem
            line-height .64rem
            margin-top .12rem
            margin-left .2rem
            color #ccc
</style>
