<template>
  <Header />
  <router-view />
  <Background />
</template>

<script setup>
import Header from "./components/Header.vue";
import Background from "./components/Background.vue";
</script>
