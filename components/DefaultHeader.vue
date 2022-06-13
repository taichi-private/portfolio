<template>
  <header class="l-header">
    <LogoItem />
    <ul class="l-header__list">
      <li class="l-header__item">about</li>
      <li class="l-header__item">works</li>
      <li class="l-header__item">contact</li>
    </ul>
  </header>
</template>

<script lang="ts">
import LogoItem from "~/components/Logo.vue";

export default {
  name: 'defaultHeader',
  components: {
    LogoItem,
  },
}
</script>

<style scoped lang="scss">
.l-header {
  display: flex;
  justify-content: space-between;
  align-content: center;
  padding: 12px 20px;
  box-shadow: 0 3px 0 #d4d4d4;

  &__list {
    display: flex;
    align-items: center;
  }
  &__item {
    margin-right: 20px;

    &:last-child {
      margin-right: 0;
    }
  }
}
</style>