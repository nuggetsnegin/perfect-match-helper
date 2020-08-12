<template>
  <div id="app">
    <div class="wrapper">
      <Header />
      <Grid/>
    </div>
    <Footer/>
  </div>
</template>

<script>
import Grid from './components/Grid'
import Header from './components/Header'
import Footer from './components/Footer'

export default {
  name: 'App',
  components: {
    Grid,
    Header,
    Footer
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

.wrapper {
  min-height: calc(100vh - 94px);
}

</style>
