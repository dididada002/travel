<template>
  <div class="icons">
    <div class="icon" v-for="item of iconList" :key="item.id">
      <div class="icon-img">
        <img
          class="icon-img-content"
          :src="item.imgSrc"
        />
      </div>
      <p class="icon-text">{{item.textContent}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeIcons",
  data() {
      return {
          iconList: [
              {
                  id:'001',
                  imgSrc:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
                  textContent:'景点门票'
              },{
                  id:'002',
                  imgSrc:'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
                  textContent:'故宫'
              },{
                  id:'003',
                  imgSrc:'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
                  textContent:'北京必游'
              },{
                  id:'004',
                  imgSrc:'http://img1.qunarzz.com/piao/fusion/1803/fa/2548667cb6e902.png',
                  textContent:'动植物园'
              },{
                  id:'005',
                  imgSrc:'http://img1.qunarzz.com/piao/fusion/1803/67/9a1678221b8e0e02.png',
                  textContent:'一日游'
              },{
                  id:'006',
                  imgSrc:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/338c5b924c5809e8c7b14f60a953c3e2.png',
                  textContent:'古北水镇'
              },{
                  id:'007',
                  imgSrc:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
                  textContent:'欢乐谷万圣节'
              },{
                  id:'008',
                  imgSrc:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
                  textContent:'赏红叶'
              }
          ]
      }
  },
};
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';

.icons {
  height: 0;
  padding-bottom: 50%;
  overflow: hidden;

  .icon {
    position: relative;
    overflow: hidden;
    width: 25%;
    height: 0;
    padding-bottom: 25%;
    float: left;

    .icon-img {
      top: 0;
      lest: 0;
      right: 0;
      bottom: 0.44rem;
      position: absolute;

      .icon-img-content {
        height: 100%;
        width: 100%;
        display: block;
        margin: 0 auto;
      }
    }

    .icon-text {
      width: 100%;
      lest: 0;
      right: 0;
      bottom: 0;
      height: 0.44rem;
      line-height: 0.44rem;
      position: absolute;
      text-align: center;
      color: $darkTextColor;
    }
  }
}
</style>