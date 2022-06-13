<template>
  <div class="p-top">
    <div class="p-top__parallax">
      <div class="p-top__mainTitle">テストです</div>
    </div>

    <section class="p-top__block p-top__block--noPadding">
      <h2 class="p-top__blockTitle">about</h2>
      <div class="p-top__panelList">
        <PanelItem :panelData="companyData" />
        <PanelItem :panelData="companyData2" :color-code="'#D8E6D8'" />
        <PanelItem :panelData="companyData3" />
      </div>
    </section>

    <div class="p-top__parallax p-top__parallax--mini"></div>

    <section class="p-top__block">
      <h2 class="p-top__blockTitle">works</h2>
    </section>

    <div class="p-top__parallax p-top__parallax--mini"></div>

    <section class="p-top__block">
      <h2 class="p-top__blockTitle">contact</h2>
    </section>

    <div class="p-top__parallax p-top__parallax--mini"></div>
  </div>
</template>

<script lang="ts">
import PanelItem from "~/components/common/PanelItem.vue"

export default {
  name: 'IndexPage',
  layout: 'default',
  components: {
    PanelItem,
  },
  data() {
    return {
      companyData: {
        title: 'ポート株式会社',
        text: '2015年1月にエンジニアで入社'
      },
      companyData2: {
        title: '株式会社ジンユウ',
        text: '2020年2月にエンジニアで入社'
      },
      companyData3: {
        title: 'コクラボ株式会社',
        text: '2021年1月にエンジニアで入社'
      },
    }
  }
}
</script>

<style scoped lang="scss">
.p-top {
  &__mainTitle {
    font-size: 40px;
    font-weight: bold;
    color: #fff;
    z-index: 2;
  }
  &__block {
    margin: 60px 0;
    padding: 0 15px;

    &--noPadding {
      margin: 60px 0 0;
      padding: 0;
    }
  }
  &__blockTitle {
    font-size: 24px;
    font-weight: bold;
    text-align: center;
  }
  &__panelList {
    margin: 20px 0 0;
    padding: 20px 0;
    background: #DFD8E6;
  }
  &__parallax {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 600px;
    background: center center no-repeat url('~/assets/images/pages/top/mv.jpg');
    background-attachment: fixed;
    background-size: cover;
    z-index: 1;

    &:after {
      position: absolute;
      top: 0;
      left: 0;
      content: '';
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.4);
    }

    &--mini {
      height: 200px;
    }
  }
}
</style>