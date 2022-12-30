<script setup>
import CashForceIconSvg from "../icons/CashForceIconSvg.vue";
import FeaturedHandShakeSvg from "../icons/FeaturedHandShakeSvg.vue";
</script>

<template>
  <nav>
    <CashForceIconSvg />
    <div className="tab-option">
      <div className="option-content">
        <FeaturedHandShakeSvg />
        <span> Notas fiscais </span>
      </div>
    </div>
  </nav>
</template>

<style scoped>
nav {
  width: 100%;
  background-color: #fbfdfe;
}

.tab-option {
  height: 64px;
  border-left: 4px #00ad8c solid;
}

.tab-option:hover {
  cursor: pointer;
}

.option-content {
  display: flex;
  align-items: center;
  height: 100%;
  column-gap: 15px;
  padding-left: 21px;
}

.option-content > span {
  font-family: "DM Sans";
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 18px;
  display: flex;
  align-items: center;

  /* P. Green / 5 */

  color: #00ad8c;
}
</style>
