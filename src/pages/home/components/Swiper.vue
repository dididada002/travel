<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="showSwiper">
      <!-- slides -->
      <swiper-slide v-for="item of list" :key="item.id">
        <img
          class="swiper-img"
          :src="item.url"
        />
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data() {
    return {
      swiperOption: {
        pagination: ".swiper-pagination"
      }
    };
  },
  computed: {
    showSwiper () {
      return this.list.length;
    }
  }
};
</script>
<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active {
  background: #ffffff;
//   给swipper下面的滑动点设置样式，必须穿透出wrapper给swipper组件设置 
}

.wrapper {
  width: 100%;
  height: 0;
  padding-bottom: 31.25%;

  .swiper-img {
    width: 100%;
  }
}
</style>