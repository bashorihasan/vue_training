<template>
  <div id="app">
    <Navbar />
    <Hero />
    <About />
    <Services />
    <Team />
    <Contact />
    <Footer />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import About from './components/About.vue'
import Services from './components/Services.vue'
import Team from './components/Team.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Hero,
    About,
    Services,
    Team,
    Contact,
    Footer
  },
  mounted() {
    console.log('Company Profile Website telah dimuat!')
    console.log('Selamat datang! 🚀')
  }
}
</script>

<style>
/* Global Styles */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

<style>
/* Global Styles */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background: #ffffff;
  color: #333;
  line-height: 1.6;
}

#app {
  width: 100%;
  overflow-x: hidden;
}

/* Smooth Scrolling */
html {
  scroll-behavior: smooth;
}

/* Section Padding */
section {
  padding: 80px 20px;
}
</style>