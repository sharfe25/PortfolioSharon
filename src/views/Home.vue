<template>
  <v-app>
    <AppBar/>
    <Welcome/>
    <Skills/>
    <About/>
    <Contact/>
    <Footer/>
  </v-app>
</template>

<script>
  import AppBar from '../components/appBar'
  import Welcome from '../components/Welcome'
  import Skills from '../components/Skills'
  import About from '../components/About'
  import Contact from '../components/Contact'
  import Footer from '../components/Footer'
  export default {
    name: 'Home',

    components: {
      AppBar,Welcome,Skills,About,Contact,Footer
    },
  }
</script>
<style scoped>

</style>