<script setup>
// import { onMounted } from 'vue'
// import AOS from 'aos'
// import 'aos/dist/aos.css'

import Heading1 from '../../Elements/Heading/Heading.vue'
import Kalimat from '../../Elements/Kalimat/paragraph.vue'

// // Inisialisasi AOS saat komponen dipasang
// onMounted(() => {
//   AOS.init({ duration: 2000 })
// })
</script>

<template>
  <div 
    data-aos="fade-up" 
    id="about" 
    class="container mx-auto my-40 px-6 sm:px-6 md:px-10 lg:px-12"
  >
    <Heading
      level = '1'
      Text="About Me" 
      Styling="text-center mb-10 text-xl capitalize sm:text-2xl md:text-4xl lg:text-6xl" 
    />
    
    <div class="text-start border p-4 sm:text-justify px-4 md:px-8 lg:px-10">
      <div class="px-2 py-2 sm:px-4 md:px-6 lg:px-6">
        <Kalimat 
          teks="saya adalah seorang pengembang Website yang berfocus pada Front End React JS menciptakan antarmuka website interaktif dan responsif dalam membangun berbagai website, kini saya mendedikasikan keahlian saya untuk membangun aplikasi front-end yang statis menggunakan React JS. Diluar hal itu saya menjalani hobby pada dunia Fotografi khususnya transportasi Bus dan Kereta Api serta menikmati perjalanan menggunakan transportasi Bus dan Kereta Api" 
          Styling="text-lg sm:text-xl md:text-1xl lg:text-2xl"
        />
      </div>
    </div>
  </div>
</template>
