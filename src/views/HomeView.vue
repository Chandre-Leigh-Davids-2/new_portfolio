<template>
  <div class="Wrapper">
    <section class="section Landing" id="main">
      <LandingComp />
    </section>

    <section class="section" id="about">
      <AboutComp />
    </section>

    <section class="section" id="resume">
      <ResumeComp />
    </section>

    <section class="section" id="projects">
      <ProjectsComp />
    </section>


    <section class="section" id="contact">
      <ContactComp />
    </section>

  </div>
</template>
<script>
import LandingComp from '@/components/Landing.vue'
import AboutComp from '@/components/About.vue'
import ResumeComp from '@/components/Resume.vue'
import ProjectsComp from '@/components/Projects.vue'
import ContactComp from '@/components/Contact.vue'
import FooterComp from '@/components/Footer.vue'



export default {
  components: {
    LandingComp,
    AboutComp,
    ResumeComp,
    ProjectsComp,
    ContactComp,
    FooterComp,
  }
}

</script>
<style scoped>
.Wrapper {
  overflow-x: hidden;
}
</style>