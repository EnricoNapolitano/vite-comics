<script>
import UpperFooter from './footer_components/UpperFooter.vue'
import DownerFooter from './footer_components/DownerFooter.vue';
export default {
    name: 'AppFooter',
    props: { icons: Array },
    components: { UpperFooter, DownerFooter }
}
</script>
<template>
    <!-- footer made of 2 components -->
    <upper-footer></upper-footer>
    <downer-footer :icons="icons"></downer-footer>
</template>
<style>

</style>