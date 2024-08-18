<template>
  <main class="main">
    <MainContent class="grid-1" />
    <RegistrationForm class="grid-3" />
    <AdditionalСontent class="grid-2" />
  </main>
</template>

<script setup>
import RegistrationForm from "@/components/RegistrationForm.vue";
import AdditionalСontent from "@/components/AdditionalСontent.vue";
import MainContent from "@/components/MainContent.vue";
</script>

<style scoped>
.main {
  position: relative;
  z-index: 10;
  max-width: 1000px;
  margin: auto;
  margin-top: 50px;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: repeat(2, 1fr);
  grid-column-gap: 0px;
  grid-row-gap: 0px;
  justify-items: center;
  align-items: center;
}
.grid-1 {
  grid-area: 1 / 1 / 2 / 2;
}
.grid-2 {
  grid-area: 2 / 1 / 3 / 2;
}
.grid-3 {
  grid-area: 1 / 2 / 3 / 3;
}
@media (max-width: 1000px) {
  .main {
    width: 820px;
  }
}
@media (max-width: 850px) {
  .main {
    margin-top: 0;
    width: 100%;
    display: flex;
    flex-direction: column;
  }
  .grid-1 {
    margin: 36px 0;
  }
  .grid-2 {
    margin-top: 36px;
    margin-bottom: 50px;
  }
}
</style>
