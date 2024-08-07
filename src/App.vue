<script setup>
import BaseHeader from "./components/BaseHeader.vue";
import BaseMain from "./components/BaseMain.vue";
import WhatsappSymbol from "./components/icons/WhatsappSymbol.vue";
</script>

<template>
  <BaseHeader />

  <main>
    <BaseMain />
    <div class="whatsapp-symbol">
      <WhatsappSymbol />
    </div>
  </main>
</template>
