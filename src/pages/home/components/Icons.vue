<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page, index) in pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgSrc" />
          </div>
          <p class="icon-text">{{item.textContent}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: "HomeIcons",
  props:{
    list: Array
  },
  data() {
    return {
      swiperOption: {
        autoplay: false
      }
    };
  },
  computed: {
    pages() {
      const pages = [];
      this.list.forEach((item, index) => {
        const page = Math.floor(index / 8);
        if (!pages[page]) {
          pages[page] = [];
        }
        pages[page].push(item);
      });
      return pages;
    }
  }
};
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';
@import '~styles/mixins.styl';

.icons >>> .swiper-container {
  height: 0;
  padding-bottom: 50%;
}

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
    ellipsis();
  }
}
</style>