<script>
import AppHeader from './components/AppHeader.vue'

export default {
  components: {
    AppHeader
  }
}
</script>

<template>
  <div class="container">
    <AppHeader />
  </div>
</template>

<style lang="scss">
@use './styles/general.scss' as *;

.container {
  max-width: 1140px;
  margin: 0 auto;
}
</style>
