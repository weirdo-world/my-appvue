<template>
  <div class="homeContainer">
    <swiper class="banner" indicator-dots autoplay="true" indicator-color="#F8F8FF" indicator-active-color="#228B22">
      <div v-for="(item,index) in bannerSrc">
        <swiper-item>
          <img :src="item" alt="" @click="toSearch" mode="scaleToFill">
        </swiper-item>
      </div>
    </swiper>
  </div>
</template>
<script>
export default {
  data () {
    return {
      bannerSrc: ['/static/images/banner/banner01.jpg', '/static/images/banner/banner02.jpg']
    }
  },
  methods: {
    toSearch () {
      wx.navigateTo({ // 跳转页面
        url: '/pages/search/main'
      })
    }
  }

}
</script>
<style>
.homeContainer {
  background-color: #F8F7FA;
}

.banner {
  margin: 10px 0;
  width: 100%;
  height: 200px;
}

.banner img {
  width: 100%;
  height: 100%;
}
</style>
