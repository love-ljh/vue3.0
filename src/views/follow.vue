<template>
  <div>
    <div class="item">
      <img :src="require('../assets/10.jpg')" alt="" />
      <div class="btns">
        <div class="follow">关注</div>
        <div class="love">点赞</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.item {
  width: 300px;
  height: 300px;
  margin: 100px auto;
  cursor: pointer;
  position: relative;
}
.item img {
  width: 100%;
  height: 100%;
  background-color: #4f4f4f;
  position: relative;
  z-index: 2;
}
.item:hover .btns {
  z-index: 3;
}
.item .btns {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1;
  background-color: rgba(0, 0, 0, 0.3);
  transition: all 0.6s;
}
.follow,
.love {
  width: 100px;
  height: 30px;
  line-height: 30px;
  text-align: center;
  border-radius: 4px;
  transition: all 0.3s;
  font-size: 14px;
  opacity: 0;
  background-color: #fff;
  color: #999;
}
.item:hover .follow {
  transform: translateY(80px);
  opacity: 1;
}
.item:hover .love {
  transform: translateY(-80px);
  opacity: 1;
}
.follow {
  position: absolute;
  left: calc(50% - 50px);
  top: -30px;
}
.love {
  position: absolute;
  bottom: -30px;
  left: calc(50% - 50px);
}
</style>