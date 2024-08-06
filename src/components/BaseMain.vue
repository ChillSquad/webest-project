<script setup></script>

<template>
  <div class="main-page">
    <div class="container">
      <div class="main-page__inner">
        <p>
          Создаём и развиваем интернет-магазины, B2B- и B2C-сервисы, обучающие
          платформы
          <span> Битрикс, Laravel, Magento, Vue.js, Flutter </span>
        </p>
      </div>
      <button>Обсудить проект</button>
    </div>
  </div>
</template>

<style scoped>
.main-page {
  width: 100%;
  height: 100vh;
  background-size: cover;
  background-image: url(../assets/img/promo-small-desktop.webp);
}

.main-page__inner {
  padding: 300px 0 0 0;
  color: #fff;
  font-size: 60px;
  font-family: "Gilroy-Black", Arial, sans-serif;
  font-weight: 900;
}

span {
  margin: 20px 0 75px 0;
  display: block;
  font-size: 20px;
}

button {
  font-family: "Gilroy-Regular", Arial, sans-serif;
  font-weight: 900;
  font-size: 18px;
  padding: 14.5px 30px;
  border: none;
  outline: none;
  cursor: pointer;
}
</style>
