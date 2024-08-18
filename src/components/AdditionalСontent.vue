<template>
  <div class="holder">
    <div class="card">
      <div class="img-holder">
        <img src="@/assets/instructor.png" alt="Кирилл Касатонов" />
      </div>
      <div class="text-holder">
        <p class="title">
          Кирилл <span style="color: #4252d1">Касатонов</span>
        </p>
        <p class="text">
          6 лет коммерческого опыта с такими компаниями как Mercedes-Benz и
          другими крупными корпорациями
        </p>
      </div>
    </div>
    <div class="card">
      <div class="img-holder">
        <img src="@/assets/box.png" alt="box" class="img_box" />
      </div>
      <div class="text-holder">
        <p class="title">Бонус за регистрацию</p>
        <p class="text">
          PDF-файл "5 преимуществ <br />
          профессии фронтенд разработчика"
        </p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.holder {
  width: 430px;
  display: flex;
  flex-direction: column;
  gap: 16px;
}
.card {
  display: flex;
  gap: 30px;
}
.img-holder {
  width: 50px;
  height: 50px;
  min-width: 50px;
}
img {
  width: 50px;
  height: 50px;
}
.img_box {
  width: 40px;
  height: 40px;
}
.title {
  font-style: normal;
  font-weight: 700;
  font-size: 14px;
  line-height: 120%;
  text-transform: uppercase;
}
.text {
  font-weight: 400;
  font-size: 12px;
  line-height: 160%;
}
@media (max-width: 850px) {
  .holder {
    flex-direction: column-reverse;
    align-items: center;
    max-width: 90vw;
  }
  .card {
    width: 280px;
    gap: 15px;
  }
}
</style>
