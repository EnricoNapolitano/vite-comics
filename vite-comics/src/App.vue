<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import BlueNav from './components/BlueNav.vue';
import AppFooter from './components/AppFooter.vue';
export default {
  name: 'DC Comics',
  components: { AppHeader, AppMain, BlueNav, AppFooter }
}
</script>


<template>
  <app-header></app-header>
  <app-main></app-main>
  <blue-nav></blue-nav>
  <app-footer></app-footer>
</template>


<style lang="scss">
@use './assets/scss/general.scss';
</style>