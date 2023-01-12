<script>
import AppHeader from './components/AppHeader.vue';
import AppCentralMenu from './components/AppCentralMenu.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    AppCentralMenu,
    AppFooter,
  }

}
</script>
<template lang="">
  <div>
    <AppHeader></AppHeader>
    <AppCentralMenu></AppCentralMenu>
    <AppFooter></AppFooter>
  </div>
</template>
<style lang="scss">
@use './styles/generals.scss' as *
</style>