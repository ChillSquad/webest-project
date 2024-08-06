<script setup>
defineProps({
  mail: {
    type: [String, null],
    default: null,
  },
});
</script>

<template>
  <a v-if="mail" :href="`mailto:${mail}`">{{ mail }}</a>
</template>
