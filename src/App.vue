<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooterTop from './components/AppFooterTop.vue';
import AppFooterBottom from './components/AppFooterBottom.vue';

export default {
  components: {
    AppHeader,
    AppMain,
    AppFooterTop,
    AppFooterBottom
  }
}
</script>

<template>

  <AppHeader />
  <AppMain />
  <AppFooterTop />
  <AppFooterBottom />

</template>

<style lang="scss">
@use './styles/general.scss' as *;

.container {
  max-width: 1270px;
  margin: 0 auto;
}
</style>
