<script setup>
defineProps({
  title: {
    type: String,
    default: null,
  },
  subtitle: {
    type: String,
    default: null,
  },
  price: {
    type: String,
    default: null,
  },
  sale: {
    type: String,
    default: null,
  },
  configurations: {
    type: Array,
    required: true,
  },
  box: {
    type: Boolean,
    default: false,
  },
});
</script>

<template>
  <section class="expertise-crm-tariff">
    <p class="expertise-crm-tariff__item-title">{{ title }}</p>

    <p class="expertise-crm-tariff__item-subtitle">
      {{ subtitle }}
    </p>

    <p class="expertise-crm-tariff__item-price">
      {{ price }} <span v-if="!box">/ мес</span>
    </p>

    <p :class="['expertise-crm-tariff__item-sale', { license: box }]">
      {{ sale }} <span v-if="!box">/ мес</span>
    </p>

    <button class="expertise-crm-tariff__item-button">Купить</button>

    <div class="expertise-crm-tariff__item-footer">
      <p
        class="icon-marker"
        v-for="(configuration, index) in configurations"
        :key="index"
      >
        {{ configuration.parameter }}
      </p>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@import "~/assets/scss/helpers/fonts-mixin";

.expertise-crm-tariff {
  &__item-title,
  &__item-price {
    margin-bottom: 8px;
  }

  &__item-button,
  &__item-sale {
    margin-bottom: 24px;
  }

  &__item-title {
    @include font-h6;
  }

  &__item-subtitle {
    @include font-text-4-1920;

    margin-bottom: 48px;
    color: var(--color-white-transparent);
  }

  &__item-price {
    @include font-h4;

    span {
      @include font-text-1;

      text-transform: lowercase;
      color: var(--color-white-transparent);
    }
  }

  &__item-sale {
    @include font-text-1;

    text-decoration: line-through;
    color: var(--color-white-transparent);
  }

  .license {
    @include font-text-4-1920;

    text-decoration: none;
  }

  &__item-button {
    padding: 24px 0;
    width: 100%;
    background: transparent;
    border: 1px solid var(--color-white);
    border-radius: 20px;
    color: var(--color-white);
    font-size: 20px;
    line-height: 20px;
    font-family: var(--ff-gilroy-semi-bold);
    cursor: pointer;
  }

  &__item-footer {
    @include font-text-4-1920;

    display: flex;
    flex-direction: column;
    gap: 8px;
    border-top: 1px solid rgba(255, 255, 255, 0.2);
    padding-top: 24px;
    color: var(--color-white-transparent);

    .icon-marker {
      display: flex;
      align-items: center;

      &:before {
        content: "\004E";
        font-size: 12px;
        color: var(--color-white);
        padding-right: 8px;
      }
    }
  }
}
</style>
