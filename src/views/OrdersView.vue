<script setup>
import HandShakeSvg from "../components/icons/HandShakeSvg.vue";
</script>

<template>
  <section className="orders-content">
    <div className="title-subtitle-wrapper">
      <div className="orders-title-container">
        <HandShakeSvg />
        <span>Notas fiscais</span>
      </div>
      <div className="orders-subtitle-container">
        <span>Visualize as notas fiscais que você tem.</span>
      </div>
    </div>
  </section>
</template>

<style scoped>
.orders-content {
  padding-left: 48px;
  padding-top: 40px;
  padding-right: 47px;
}

.title-subtitle-wrapper {
  display: flex;
  flex-direction: column;
  row-gap: 5px;
}

.orders-title-container {
  display: flex;
  align-items: center;
  column-gap: 9px;
}

.orders-subtitle-container {
  font-family: "DM Sans";
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  color: #727d94;
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
