<script setup>
defineProps({
  urlImage: {
    type: String,
    default: null,
  },
  title: {
    type: String,
    default: null,
  },
});
</script>

<template>
  <div class="main-slider-card">
    <img
      class="main-slider-card__story-image"
      :src="urlImage"
      alt="story image"
    />
    <p class="main-slider-card__story-heading">
      {{ title }}
    </p>
  </div>
</template>
