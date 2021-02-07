<template>
  <div class="homeContainer">
    <swiper class="banner" indicator-dots autoplay="true" indicator-color="#F8F8FF" indicator-active-color="#228B22">
      <div v-for="item in bannerSrc">
        <swiper-item>
          <img :src="item" alt="" @click="toSearch" mode="scaleToFill">
        </swiper-item>
      </div>
    </swiper>
    <div class="shop-body">
      <p class="shop-title">产品展示</p>
      <div class="product" v-for="item in productImg">
        <img :src="item.url" mode="aspectFit">
        <p>名称：<span>{{ item.title }}</span></p>
        <p>价格：<span>{{ item.pric }}</span></p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
      bannerSrc: ['/static/images/banner/banner-01.jpg', '/static/images/banner/banner-02.jpg'],
      productImg: [
        {url: '/static/images/shop/01.jpg', title: '名称一', pric: '￥666'},
        {url: '/static/images/shop/02.jpg', title: '名称二', pric: '￥999'},
        {url: '/static/images/shop/03.jpg', title: '名称三', pric: '￥888'},
        {url: '/static/images/shop/04.jpg', title: '名称四', pric: '￥699'},
        {url: '/static/images/shop/05.jpg', title: '名称五', pric: '￥12000'}
      ]
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
  color: #1D1D1F;
  padding-bottom: 30px;
}

.banner {
  margin-bottom: 10px;
  width: 100%;
  height: 200px;
}

.banner img {
  width: 100%;
  height: 100%;
}

.shop-body {
  width: 100%;
  padding-bottom: 20px;
}

.shop-body .shop-title {
  width: 100%;
  height: 30px;
  text-align: center;
  letter-spacing: 5px;
  font-size: 24px;
  font-weight: bold;

}

.shop-body .product {
  width: 40%;
  float: left;
  margin: 10px;
  padding: 0 5px;
  background-color: white;
}

.shop-body .product img {
  width: 100%;
}

.shop-body .product p {
  padding: 5px;
  text-align: left;
  color: #1D1D1F;
  font-size: 14px;
  font-weight: bold;
}

.shop-body .product p span {
  font-weight: normal;
}
</style>
