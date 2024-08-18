<template>
  <header>
    <img src="@/assets/logo.png" alt="Powercode Academy" class="logo" />
    <div class="items-holder">
      <div class="table-item">
        <i class="pi pi-calendar"></i>
        <p>28 декабря</p>
      </div>
      <div class="table-item">
        <i class="pi pi-clock"></i>
        <p>3,5 часа</p>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  position: relative;
  margin-top: 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: min(1040px, 90%);
  height: 104px;
  padding: 24px 56px;
  margin: auto;
  box-sizing: border-box;
  z-index: 10;
}
.logo {
  height: 56px;
}
.items-holder {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 18px;
}
@media (max-width: 850px) {
  header {
    width: 100%;
    padding: 2rem;
  }
}
@media (max-width: 570px) {
  header {
    width: 100%;
    padding: 1rem;
  }
  .items-holder {
    gap: 8px;
  }
  .logo {
    height: 32px;
  }
}
</style>
