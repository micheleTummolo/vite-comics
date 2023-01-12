<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';
import AppCentralMenu from './components/AppCentralMenu.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    AppContent,
    AppCentralMenu,
    AppFooter,
  }

}
</script>
<template lang="">
  <div>
    <AppHeader></AppHeader>
    <AppContent></AppContent>
    <AppCentralMenu></AppCentralMenu>
    <AppFooter></AppFooter>
  </div>
</template>
<style lang="scss">
@use './styles/generals.scss' as *
</style>