<template>
  <header>
    <MainHeader />
  </header>
  <main>
    <Main />
  </main>
  <footer>
    <MainFooter />
  </footer>
</template>

<script>
import MainHeader from './components/header.vue'
import Main from './components/main.vue'
import MainFooter from './components/footer.vue'

export default {
  name: 'App',
  components: {
    MainHeader,
    Main,
    MainFooter
  }
}
</script>

<style scoped>
@import url(./assets/style.css);
</style>