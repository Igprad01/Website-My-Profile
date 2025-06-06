<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'
// import AOS from 'aos'
// import 'aos/dist/aos.css'

import Heading from '../../elements/Heading/Heading.vue'
import Kalimat from '../../elements/Kalimat/paragraph.vue'

// Data dan state
const TextRunning = ['front end developer', 'data engineer']
const textIndex = ref(0)

let intervalId = null

onMounted(() => {
  // AOS.init({ duration: 2000 })

  intervalId = setInterval(() => {
    textIndex.value = (textIndex.value + 1) % TextRunning.length
  }, 2000) // ganti interval jadi 2 detik agar tidak terlalu cepat
})

onBeforeUnmount(() => {
  if (intervalId) clearInterval(intervalId)
})
</script>

<template>
  <div
    id="home"
    data-aos="fade-up"
    class="container mx-auto px-4 sm:px-6 lg:px-8 py-8"
  >
    <div>
      <Heading
        :level="1"
        text="putra pradwi."
        Styling="font-bold text-3xl mb-10 capitalize sm:text-4xl lg:text-5xl mb-6"
      />
      <Heading
        :level="2"
        :text="TextRunning[textIndex]"
        Styling="font-bold capitalize text-xl mb-10 sm:text-2xl lg:text-6xl mb-7 transition-opacity duration-500 ease-in-out"
      />
      <div>
        <Kalimat
          teks="2 tahun berpengalaman dalam dunia programming, dimulai dengan PHP untuk membangun website dinamis, lalu beralih ke C++ guna mempelajari dasar-dasar pemrograman. Saat ini sedang fokus pada React JS, khususnya dalam pengembangan website front-end"
          Styling="italic text-xl text-justify sm:text-xl text-start lg:text-2xl"
        />
      </div>
    </div>
  </div>
</template>
