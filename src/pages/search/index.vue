<template>
  <div class="homeContainer">
    <div class="search-top">
      <img src="/static/images/search.png">
      <input confirm-type="search" placeholder="输入名称搜索">
    </div>
  </div>
</template>

<script>
export default {
  name: 'index'
}
</script>

<style scoped>
.search-top {
  display: flex;
  width: 80%;
  margin: auto;
  height: 30px;
  padding: 3px;
  border-bottom: 1px solid #ff4500;

}

.search-top img {
  width: 30px;
  height: 30px;
}

.search-top input {
  height: 30px;
  width: 100%;
  padding-left: 10px;
}
</style>
