<script setup>
import ArrowUpRight from "./icons/ArrowUpRight.vue";

defineProps({
  imagePath: String,
  title: String,
  text: String,
});
</script>

<template>
  <div class="card">
    <picture class="card__picture">
      <img :src="imagePath" alt="cordian image" />
    </picture>
    <h3 class="card__title">
      {{ title }}
      <span class="card__title--arrow"><ArrowUpRight /></span>
    </h3>
    <h6 class="card__footnote">{{ text }}</h6>
  </div>
</template>
