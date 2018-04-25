<template>
    <div id="app">
      <AppHeader></AppHeader>
      <AppNavBar></AppNavBar>
      <AppContent></AppContent>
      <AppFooter></AppFooter>

    </div>
</template>

<script>
import AppHeader from './components/AppHeader'
import AppNavBar from './components/AppNavBar'
import AppContent from './components/AppContent'
import AppFooter from './components/AppFooter'

export default {
  name: 'app',
  components: {
      AppHeader,
      AppNavBar,
      AppContent,
      AppFooter
  }
}
</script>

<style lang="scss">
@import './styles/reset.scss';
@import './styles/type.scss';

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

li {
  display: inline-block;
  margin: 0 10px;
}


</style>
