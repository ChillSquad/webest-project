<script setup>
import CaseUnitPlate from "./CaseUnitPlate.vue";
import { useSidebarModel } from "../models/sidebar";

const { toggleSidebarFormCase } = useSidebarModel();

defineProps({
  urlImage: {
    type: String,
    default: null,
  },
  title: {
    type: String,
    default: null,
  },
  hasData: {
    type: Boolean,
    default: false,
  },
  textColor: {
    type: String,
    default: "#000",
  },
  wide: {
    type: Boolean,
    default: false,
  },
  article: {
    type: Boolean,
    default: false,
  },
  slider: {
    type: Boolean,
    default: false,
  },
  moreData: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <div class="case-unit-card">
    <div :class="['case-unit-card__inner', { right: wide }]">
      <NuxtLink to="/case/article">
        <img
          :class="['case-unit-card__case-image', { sliding: slider }]"
          :src="urlImage"
          :alt="urlImage"
        />

        <p :style="{ color: textColor }" class="case-unit-card__case-heading">
          {{ title }}
        </p>
      </NuxtLink>

      <button
        @click="toggleSidebarFormCase"
        class="case-unit-card__case-button"
      >
        <span>i</span>
      </button>

      <CaseUnitPlate v-if="hasData" :items="moreData" :platePosition="wide" />
    </div>
  </div>
</template>
