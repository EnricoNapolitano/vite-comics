<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
export default {
  name: 'DC Comics',
  components: { AppHeader, AppMain, AppFooter }
}
</script>


<template>
  <app-header></app-header>
  <app-main></app-main>
  <app-footer></app-footer>
  <footer></footer>
</template>


<style lang="scss">
@use './assets/scss/general.scss';
</style>