<script setup>
defineProps({
  phone: {
    type: [String, null],
    default: null,
  },
});
</script>

<template>
  <a v-if="phone" :href="`tel:${phone}`">{{ phone }}</a>
</template>
