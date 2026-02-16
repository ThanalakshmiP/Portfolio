<template>
  <div id="app">
    <Navigation />
    <Hero />
    <Experience />
    <Projects />
    <Contact />
  </div>
</template>

<script>
import Navigation from './components/Navigation.vue'
import Hero from './components/Hero.vue'
import Experience from './components/Experience.vue'
import Projects from './components/Projects.vue'
import Contact from './components/Contact.vue'

export default {
  name: 'App',
  components: {
    Navigation,
    Hero,
    Experience,
    Projects,
    Contact
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  line-height: 1.6;
  color: #333;
}

@media (max-width: 768px) {
  .hero {
    flex-direction: column;
    padding: 40px 20px;
  }

  .hero h1 {
    font-size: 36px;
  }

  .yellow-blob {
    width: 400px;
    height: 400px;
  }

  .hero-photo {
    width: 100%;
    max-width: 350px;
    height: 400px;
  }

  .projects {
    padding: 60px 20px;
  }

  .project-card {
    flex-direction: column !important;
    padding: 30px 20px;
  }

  .project-image {
    width: 100%;
  }
}
</style>
