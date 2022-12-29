<script setup>
import HandShakeSvg from "../components/icons/HandShakeSvg.vue";
</script>

<template>
  <section className="orders-content">
    <div className="orders-title-container">
      <HandShakeSvg />
      <span>Notas fiscais</span>
    </div>
  </section>
</template>

<style scoped>
.orders-content {
  padding-left: 48px;
  padding-top: 40px;
  padding-right: 47px;
}

.orders-title-container {
  display: flex;
  align-items: center;
  column-gap: 9px;
}

.orders-title-container > span {
  font-family: "DM Sans";
  color: #021b51;
  font-style: normal;
  font-weight: 700;
  font-size: 24px;
  line-height: 28px;
}
</style>
