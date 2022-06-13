<template>
  <div class="c-panel" :style="styles">
    <div class="c-panel__inner">
      <div class="c-panel__content">
        <h3 class="c-panel__title">{{ panelData.title }}</h3>
        <p class="c-panel__text">{{ panelData.text }}</p>
      </div>
      <img class="c-panel__img" src="~/assets/images/pages/top/port.jpg" alt="">
    </div>
  </div>
</template>

<script lang="ts">
type DropdownStyles = {
  '--bg-color'?: String
};
export default {
  name: 'PanelItem',
  props: {
    panelData: {
      type: Object,
      default: () => {},
      required: true,
    },
    colorCode: {
      type: String,
      default: '',
    }
  },
  computed: {
    styles(): DropdownStyles {
      return {
        '--bg-color': (this as any).colorCode
      }
    }
  }
}
</script>

<style scoped lang="scss">
.c-panel {
  padding: 20px 0;
  width: 100%;
  background: var(--bg-color);

  &:nth-of-type(even) {
    .c-panel__inner {
      flex-direction: row-reverse;
    }
  }

  &__inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 80%;
    margin: 0 auto;
  }
  &__img {
    width: 400px;
    height: 400px;
    object-fit: cover;
  }
}
</style>