<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
export default {
  name: 'DC Comics',
  components: { AppHeader, AppMain }
}
</script>


<template>
  <app-header></app-header>
  <app-main></app-main>
  <footer></footer>
</template>


<style lang="scss">
@use './assets/scss/general.scss';
</style>