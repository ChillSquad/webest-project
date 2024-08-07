<script setup>
import CompanyPhone from "./CompanyPhone.vue";
import CompanyMail from "./CompanyMail.vue";
import IconBurgerMenu from "./icons/IconBurgerMenu.vue";
</script>

<template>
  <header class="header">
    <div class="container header__inner">
      <a href="webest-project/src/App.vue">
        <img src="../assets/img/logo.png" alt="webest-logo" />
      </a>
      <a href="webest-project/src/App.vue" class="header__name">webest</a>

      <div class="header__contacts">
        <CompanyPhone phone="+7 (495) 128-22-90" />

        <CompanyMail mail="info@webest.ru" />
      </div>

      <button type="button" class="header__burger"><IconBurgerMenu /></button>
    </div>
  </header>
</template>
