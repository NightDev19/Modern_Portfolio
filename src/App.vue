<template>
  <div id="app" class="bg-neutral-900">
    <Navbar />
    <Home />
    <About />
    <Skills />
    <div class="flex flex-col md:flex-row" id="experience education">
      <Experience />
      <Education />
    </div>
    <Projects />
    <Footer />
  </div>
</template>

<script>
import Navbar from "./components/ui/Navbar.vue";
import Home from "./views/Home.vue";
import About from "./views/About.vue";
import Footer from "./views/Footer.vue";
import Experience from "./views/Experience.vue";
import Education from "./views/Education.vue";
import Skills from "./views/Skills.vue";
import Projects from "./views/Projects.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Home,
    About,
    Skills,
    Experience,
    Education,
    Projects,
    Footer,
  },
};
</script>
