<script>
import AppHeader from './components/header/AppHeader.vue';
import AppMain from './components/main/AppMain.vue';
import AppFooter from './components/footer/AppFooter.vue';
import videos from './data/videos.js'
import blogs from './data/blogs.js'
import pictures from './data/pictures.js'
export default {
  name: 'instrumental-rock',
  components: { AppHeader, AppMain, AppFooter },
  data() {
    return {
      videos, blogs, pictures
    }
  }
}
</script>

<template>
  <app-header></app-header>
  <app-main :videos="videos" :blogs="blogs" :pictures="pictures"></app-main>
  <app-footer></app-footer>
</template>

<style lang="scss">
@use './assets/scss/style.scss';
</style>