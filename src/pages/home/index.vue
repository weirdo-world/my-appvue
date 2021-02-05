<template>
  <div class="homeContainer">
    <div class="search-top">
      <img src="/static/images/search.png">
      <input confirm-type="search" placeholder="输入名称搜索">
    </div>
    <swiper class="banner" indicator-dots autoplay="true" indicator-color="#F8F8FF" indicator-active-color="#228B22">
      <swiper-item>
        <img src="/static/images/banner/banner01.jpg" mode="scaleToFill">
      </swiper-item>
      <swiper-item>
        <img src="/static/images/banner/banner02.jpg" mode="scaleToFill">
      </swiper-item>
      <swiper-item>
        <img src="/static/images/banner/banner01.jpg" mode="scaleToFill">
      </swiper-item>
      <swiper-item>
        <img src="/static/images/banner/banner02.jpg" mode="scaleToFill">
      </swiper-item>
    </swiper>
  </div>
</template>
<script>
export default {}
</script>
<style>
.homeContainer {
  background-color: #F8F7FA;
}
.search-top{
  display: flex;
  width: 80%;
  margin: auto;
  height: 60rpx;
  padding: 10rpx;
  border-bottom: 3rpx solid #ff4500;

}
.search-top img{
  width: 60rpx;
  height: 60rpx;
}
.search-top input{
  height: 60rpx;
  width: 100%;
  padding-left: 10rpx;
}
.banner{
  margin: 10rpx 0;
  width: 100%;
  height: 350rpx;
}
.banner img{
  width: 100%;
  height: 100%;
}
</style>
