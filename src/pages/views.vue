<script setup>
import Navbar from '@/components/Layouts/Navbar/Navbar.vue'
import HeroSection from '@/components/Layouts/Hero_Section/Hero_section.vue'
import About from '@/components/Layouts/About_Me/About_Me.vue'
import SectionProject from '@/components/Layouts/Project_Section/Project_section.vue'
import Sertifikat from '@/components/Layouts/Section_Certification/Section_Certification.vue'
import Footer from '@/components/Layouts/Footer/Footer.vue'

// import AOS from 'aos'
// import 'aos/dist/aos.css'
// import { onMounted } from 'vue'

// onMounted(() => {
//   AOS.init()
// })
</script>

<template>
  <div class="font-montserrat">
    <Navbar />
    <HeroSection />
    <About />
    <SectionProject />
    <Sertifikat />
    <Footer />
  </div>
</template>
