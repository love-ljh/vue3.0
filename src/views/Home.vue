<template>
  <div class="home">
    <div class="box">
      <img :src="require('../assets/10.jpg')" alt="Kitty的头像" />
      <div class="box2">
        <h3>Kitty的头像</h3>
        <p>Kitty的名字</p>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  components: {

  }
};
</script>
<style scoped leng="scss">
.box {
  position: relative;
  z-index: 1;
  display: inline-block;
  overflow: hidden;
  background: #3085a3;
  text-align: center;
  cursor: pointer;
}
.box img {
  width: 200px;
  height: 200px;
  opacity: 1;
  transition: opacity 0.35s, transform 0.35s;
  float: left;
}
.box:hover img {
  opacity: 0.5;
}
.box h3 {
  margin-top: 20%;
  transition: transform 0.35s;
  transform: translate3d(0, 20px, 0);
  opacity: 0;
  color: #fff;
  font-size: 16px;
}
.box p {
  margin: 10px 0 0;
  padding: 15px;
  border: 1px solid #fff;
  opacity: 0;
  transition: opacity 0.35s, transform 0.35s;
  transform: translate3d(0, 20px, 0) scale(1.1);
  color: #fff;
}
.box:hover h3 {
  transform: translate3d(0, 0, 0);
  opacity: 1;
}
.box:hover p {
  opacity: 1;
  transform: translate3d(0, 0, 0) scale(1);
}
.box2 {
  width: 200px;
  height: 200px;
  padding: 15px;
  position: absolute;
  box-sizing: border-box;
}
</style>
