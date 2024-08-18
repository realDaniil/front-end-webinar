<template>
  <div class="background">
    <div class="circle circle_1"></div>
    <div class="circle circle_2"></div>
    <div class="circle circle_3"></div>
    <div class="icons-holder">
      <img src="@/assets/js.png" class="js" alt="js" />
      <img src="@/assets/css.png" class="css" alt="css" />
      <img src="@/assets/html.png" class="html" alt="html" />
      <img src="@/assets/vs.png" class="vs" alt="vs" />
      <img src="@/assets/sublime.png" class="sublime" alt="sublime" />
    </div>
    <p class="text">front-end developer</p>
  </div>
</template>

<style scoped lang="scss">
.background {
  position: absolute;
  top: 0;
  height: 100vh;
  width: 100%;
  max-width: 100%;
  overflow: hidden;
  z-index: 1;
}
.circle {
  position: fixed;
  border-radius: 50%;
  background: #332f65;
}
.circle_1 {
  width: 400px;
  height: 400px;
  opacity: 0.5;
  filter: blur(111.131px);
  left: -31.33px;
  top: -70px;
  bottom: 489.69px;
}
.circle_2 {
  width: 790.65px;
  height: 793.23px;
  left: 1068.67px;
  bottom: 342.77px;
  opacity: 0.8;
  filter: blur(103.131px);
  transform: rotate(9.41deg);
}
.text {
  position: absolute;
  font-weight: 800;
  text-transform: uppercase;
  font-size: 8.95vw;
  -webkit-text-stroke: 1px rgba(255, 255, 255, 0.05);
  color: transparent;
  line-height: 7vw;
  bottom: 0;
}
.icons-holder img {
  position: absolute;
}
.html {
  width: 88.28px;
  bottom: 473px;
  right: 36px;
}
.js {
  width: 61.89px;
  bottom: 328px;
  right: 36px;
}
.sublime {
  width: 53.93px;
  bottom: 269px;
  right: 152px;
}
.css {
  width: 60.4px;
  bottom: 376px;
  right: 133px;
}
.vs {
  width: 60.62px;
  bottom: 194px;
  right: 65px;
}
@media (max-width: 850px) {
  .circle_1,
  .text,
  .icons-holder {
    display: none;
  }
  .circle_2 {
    position: relative;
    width: 512px;
    height: 512px;
    left: 351px;
    top: 910px;
    filter: blur(250px);
  }
  .background {
    height: 1200px;
  }
}
</style>
