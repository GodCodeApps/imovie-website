<template>
  <Header/>
  <SubTitle msg="Welcome to Your iMovie"/>
</template>

<script>
import Header from './components/Header.vue'
import SubTitle from './components/Home.vue'

export default {
  name: 'App',
  components: {
    Header,
    SubTitle
  }

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
