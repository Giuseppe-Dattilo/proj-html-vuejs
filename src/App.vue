<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import videos from './data/videos.js'
export default {
  name: 'instrumental-rock',
  components: { AppHeader, AppMain, AppFooter },
  data() {
    return {
      videos
    }
  }
}
</script>

<template>
  <app-header></app-header>
  <app-main :videos="videos"></app-main>
  <app-footer></app-footer>
</template>

<style lang="scss">
@use './assets/scss/style.scss';
</style>