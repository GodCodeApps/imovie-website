<template>
  <Header/>
  <Body msg="Welcome to Your iMovie"/>
  <Footer/>
</template>

<script>
import Header from './components/header.vue'
import Body from './components/body.vue'
import Footer from './components/footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Body,
    Footer
  },
  methods: {}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  width: 100%;
  height: 100%;
  margin: 0;
}
</style>
