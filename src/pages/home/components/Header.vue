<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont back-icon">&#xe65c;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe63c;</span>
      输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{this.city}}
        <span class="iconfont">&#xe643;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: {
    city: String
  }
};
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';

.header {
  display: flex;
  line-height: 0.86rem;
  background-color: $bgColor;
  color: #fff;

  .header-left {
    width: 0.64rem;
    float: left;

    .back-icon {
      text-align: center;
      font-size: 0.5rem;
    }
  }

  .header-right {
    width: 1.24rem;
    float: right;
    text-align: center;
  }

  .header-input {
    flex: 1;
    background-color: #fff;
    border-radius: 0.1rem;
    padding-left: 0.2rem;
    height: 0.64rem;
    line-height: 0.64rem;
    margin-top: 0.12rem;
    margin-left: 0.2rem;
    color: #ccc;
  }
}
</style>
