<script setup>
import CompanyPhone from "./CompanyPhone.vue";
import CompanyMail from "./CompanyMail.vue";
</script>

<template>
  <header class="header">
    <div class="container header__inner">
      <div class="header__logo">Webest</div>

      <div class="header__contacts">
        <CompanyPhone phone="+7 (495) 128-22-90" />

        <CompanyMail mail="info@webest.ru" />
      </div>

      <button type="button" class="header__burger">☰</button>
    </div>
  </header>
</template>
