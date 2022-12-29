<script setup>
import HeaderCashforce from "../header/HeaderCashforce.vue";
import { RouterView } from "vue-router";
</script>

<template>
  <section className="main">
    <HeaderCashforce />
    <RouterView />
  </section>
</template>

<style scoped>
.main {
  background-color: white;
  width: 100%;
  height: 100vh;
}
</style>
