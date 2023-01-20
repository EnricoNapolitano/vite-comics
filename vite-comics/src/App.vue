<script>
import AppHeader from './components/AppHeader.vue';
export default {
  name: 'DC Comics',
  components: { AppHeader }
}
</script>


<template>
  <app-header></app-header>
  <main></main>
  <footer></footer>
</template>


<style lang="scss">
@use './assets/scss/general.scss';
</style>