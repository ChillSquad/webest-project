<script setup>
import ArrowDown from "./icons/ArrowDown.vue";
import ScrollDown from "./icons/ScrollDown.vue";
</script>

<template>
  <div class="main-page">
    <div class="container">
      <div class="main-page__inner">
        <p>
          Создаём и развиваем интернет-магазины, B2B- и B2C-сервисы, обучающие
          платформы
          <span> Битрикс, Laravel, Magento, Vue.js, Flutter </span>
        </p>
        <div class="scroll">
          <ScrollDown />
        </div>
        <div class="arrow"><ArrowDown /></div>
      </div>
      <button type="button">Обсудить проект</button>
    </div>
  </div>
</template>
