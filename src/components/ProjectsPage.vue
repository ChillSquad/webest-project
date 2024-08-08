<script setup>
import CardsList from "./CardsList.vue";
</script>

<template>
  <div class="project-page">
    <div class="container">
      <div class="project-page__inner">
        <div class="project-page__header">
          <h1>Проекты</h1>
          <h3>
            Топ-10 России по eCommerce
            <span
              >по версии рейтинга рунета 2022 года. Помогаем клиентам создавать
              новые и улучшать существующие IT-продукты. Реализовали более 100
              проектов.
            </span>
          </h3>
          <CardsList />
        </div>
      </div>
    </div>
  </div>
</template>
