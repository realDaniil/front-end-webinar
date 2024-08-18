<template>
  <div class="holder">
    <div class="table-item">
      <i class="pi pi-globe"></i>
      <p>Вебинар</p>
    </div>
    <h1 class="text-red">FRONT-END</h1>
    <div class="back-red">
      <p>С НУЛЯ</p>
      <div class="inverted"></div>
    </div>
    <p class="white-text">легкий старт в IT профессии</p>
    <p class="main-text">
      Узнайте какими
      <span> навыками должен обладать фронтенд разработчик в 2022 году </span> и
      как начать карьеру в востребованной профессии
    </p>
  </div>
</template>

<style scoped lang="scss">
.holder {
  width: 430px;
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.table-item {
  background: rgb(66, 82, 209);
}
.text-red {
  color: rgb(255, 52, 89);
  font-weight: 800;
  font-size: 77px;
  line-height: 96px;
  text-transform: uppercase;
  font-weight: 800;
}

.back-red {
  position: absolute;
  display: inline;
  left: 14px;
  top: 135px;
  p {
    position: relative;
    z-index: 1;
    font-size: 23px;
    font-weight: 800;
    line-height: 28.75px;
    text-align: left;
  }
  .inverted {
    top: -7px;
    left: -12px;
    z-index: 0;
    position: absolute;
    background: #ff3459;
    width: 107px;
    height: 40px;
    border-radius: 5px;
    transform: rotate(-3.51deg);
  }
}
.white-text {
  font-size: 22px;
  font-weight: 600;
  line-height: 26.95px;
  text-align: left;
  position: relative;
  left: 55px;
  display: inline;
}

.main-text {
  margin-top: 30px;
  font-size: 18px;
  font-weight: 400;
  line-height: 26.64px;
  text-align: left;
  span {
    font-weight: 600;
  }
}
@media (max-width: 850px) {
  .text-red {
    font-size: 54px;
    text-align: center;
    line-height: 66px;
  }
  .back-red {
    left: 70px;
    top: 105px;
    p {
      font-size: 16px;
      line-height: 20px;
    }
    .inverted {
      width: 76px;
      height: 27px;
      top: -3px;
      left: -8px;
    }
  }
  .table-item {
    margin: auto;
  }
  .white-text {
    font-size: 16px;
    line-height: 18px;
    left: 40px;
  }
  .main-text {
    text-align: center;
    font-size: 16px;
    max-width: 400px;
  }
}
@media (max-width: 570px) {
  .back-red {
    top: 90px;
  }
}
</style>
