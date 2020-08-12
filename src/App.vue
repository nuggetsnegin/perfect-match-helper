<template>
  <div id="app">
    <Header />
    <Grid/>
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

body {
  min-height: 100%;
  display: grid;
  grid-template-rows: 1fr auto;
}

footer {
  grid-row-start: 2;
  grid-row-end: 3;
}

</style>
