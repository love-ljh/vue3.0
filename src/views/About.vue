<template>
  <div class="about">
    <div class="lists">
      <div class="item">
        <div class="text">
          <h1>标题名称</h1>
          <img :src="require('../assets/10.jpg')" />
          <h2 class="animate-text">Kitty 的测试案例</h2>
          <p class="animate-text">
            这里放内容简介，内容简介,这里放内容简介，内容简介,这里放内容简介，内容简介
          </p>
          <div class="dots"><span></span> <span></span> <span></span></div>
        </div>
      </div>
    </div>
  </div>
</template>
<style  scoped>
* {
  margin: 0;
  padding: 0;
}
.lists {
  width: 100%;
  display: flex;
  justify-content: center;
  margin-top: 100px;
}
.item {
  width: 300px;
  height: 300px;
  background-color: #99aeff;
  position: relative;
  cursor: pointer;
  transition: all 0.4s ease-out;
  box-shadow: 0px 35px 77px -17px rgba(0, 0, 0, 0.44);
  overflow: hidden;
  color: #fff;
}
.item img {
  height: 100%;
  width: 100%;
  position: absolute;
  top: 0;
  left: 0;
  z-index: 0;
  transition: all 0.4s ease-out;
}
.item .text {
  width: 100%;
  height: 100%;
  box-sizing: border-box;
  z-index: 99;
  position: absolute;
  padding: 30px;
}
.item h1 {
  text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.3);
}
.item h2 {
  margin-top: 20px;
  font-style: italic;
  transform: translateX(200px);
}
.item p {
  margin-top: 20px;
  line-height: 25px;
  transform: translateX(-200px);
  transition-delay: 0.2s;
}
.animate-text {
  opacity: 0;
  transition: all 0.6s ease-in-out;
}
.item:hover {
  box-shadow: 0px 35px 77px -17px rgba(0, 0, 0, 0.64);
  transform: scale(1.05);
}
.item:hover img {
  opacity: 0.2;
}
.item:hover .animate-text {
  transform: translateX(0);
  opacity: 1;
}
.dots {
  position: absolute;
  bottom: 20px;
  right: 30px;
  margin: 0 auto;
  width: 30px;
  height: 30px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
}
.dots span {
  width: 5px;
  height: 5px;
  background-color: #fff;
  border-radius: 50%;
  display: block;
  opacity: 0;
  transition: transform 0.4s ease-out, opacity 0.5s ease;
  transform: translateY(30px);
}
.item:hover span {
  opacity: 1;
  transform: translateY(0px);
}
.dots span:nth-child(1) {
  transition-delay: 0.05s;
}
.dots span:nth-child(2) {
  transition-delay: 0.1s;
}
.dots span:nth-child(3) {
  transition-delay: 0.15s;
}
</style>
