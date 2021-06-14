<template>
  <section>
    <Navigation />
    <Heading />
  </section>
</template>

<script>
import Navigation from './components/Navigation.vue'
import Heading from './components/Heading.vue'

export default {
  name: 'App',
  components: {
    Navigation,
    Heading
  }
}
</script>

<style>
html, body {
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 62.5%;
  color: #111;
  background: #fafafa;
}
</style>
