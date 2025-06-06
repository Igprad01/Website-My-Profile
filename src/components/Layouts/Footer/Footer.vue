<script setup>
// import { onMounted } from 'vue'
// import AOS from 'aos'
// import 'aos/dist/aos.css'

import Heading1 from '../../Elements/Heading/Heading.vue'
import Heading2 from '../../Elements/Heading/Heading.vue'
import ExternalLink from '../../Elements/ExternalLink/Tautan.vue'
// import Image from '../../image/Image.vue'

// onMounted(() => {
//   AOS.init({ duration: 2000 })
// })
</script>

<template>
  <footer data-aos="fade-up" class="mx-auto py-40 bg-slate-900">
    <div class="container mx-auto px-4 py-8 sm:px-6 lg:px-8">
      <Heading 
        level = '1'
        Text="Mau nongki Hingga Berdiskusi ide seru? atau membicarakan terkait sesuatu yang lain?"
        Styling="text-3xl sm:text-6xl md:text-7xl lg:text-6xl"
      />

      <div class="my-12 mx-auto">
        <Image src="/img/marin.png" styleImg="w-60 rounded-full" />
        <Heading
         level = '2'
          Text="Contact Me"
          Styling="text-2xl mt-5 ml-4 sm:text-4xl lg:text-5xl"
        />

        <div class="flex flex-col text-center mt-5">
          <!-- LinkedIn -->
          <div class="flex flex-row gap-5 justify-center items-center">
            <a
              href="https://www.linkedin.com/in/i-gusti-bagus-putra-pradwi/"
              target="_blank"
              rel="noopener noreferrer"
            >
              <img
                src="https://cdn-icons-png.flaticon.com/512/174/174857.png"
                alt="LinkedIn"
                class="w-5 h-5 sm:w-6 sm:h-6 md:w-8 md:h-8 lg:w-10 lg:h-10"
              />
            </a>
            <ExternalLink
              konten="I Gusti Bagus Putra Pradwi"
              href="https://www.linkedin.com/in/i-gusti-bagus-putra-pradwi/"
              styling="text-xl sm:text-2xl md:text-3xl lg:text-3xl"
            />
          </div>

          <!-- Twitter -->
          <div class="flex flex-row gap-5 mt-3 justify-center items-center">
            <a
              href="https://x.com/IPradwi"
              target="_blank"
              rel="noopener noreferrer"
            >
              <img
                src="https://cdn-icons-png.flaticon.com/512/733/733579.png"
                alt="Twitter"
                class="w-5 h-5 sm:w-6 sm:h-6 md:w-8 md:h-8 lg:w-10 lg:h-10"
              />
            </a>
            <ExternalLink
              konten="I Gusti Bagus Putra Pradwi"
              href="https://x.com/IPradwi"
              styling="text-xl sm:text-2xl md:text-3xl lg:text-3xl"
            />
          </div>
        </div>
      </div>
    </div>

    <!-- Optional Footer Bottom -->
    <!-- <div>
      <Heading1 Text="Terima Kasih Telah Berkunjung" Styling="text-center text-white text-xl mt-10" />
    </div> -->
  </footer>
</template>
