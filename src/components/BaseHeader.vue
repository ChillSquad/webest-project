<script setup>
import CompanyPhone from "./CompanyPhone.vue";
</script>

<template>
  <header class="header">
    <div class="container header__inner">
      <div class="header__logo">Webest</div>

      <div class="header__contacts">
        <CompanyPhone phone="+7 (000) 000-00-00" />

        <a class="page-header__link" href="mailto:info@webest.ru">
          info@webest.ru
        </a>
      </div>

      <button type="button" class="header__burger"></button>
    </div>
  </header>
</template>
