<template>
    <div class="search">
        <input class="search-input" type="text" placeholder="输入城市名或拼音"/>
    </div>
</template>

<script>
export default {
    name: 'CitySearch'
}
</script>

<style scoped lang="stylus">
@import '~styles/varibles.styl';
    .search {
        height .72rem
        padding 0 .1rem
        background-color $bgColor

        .search-input {
            box-sizing border-box
            padding 0 .1rem
            height .62rem
            width 100%
            line-height .62rem
            text-align center
            border-radius .06rem
            color #666
        }
    }
</style>