<script setup>
import { onMounted, ref } from 'vue'
// import AOS from 'aos'
// import 'aos/dist/aos.css'

import Card from '@/components/Elements/Card/Card.vue'
import Heading1 from '@/components/Elements/Heading/Heading.vue'

// onMounted(() => {
//   AOS.init({ duration: 2000 })
// })

const cards = ref([
  {
    id: 1,
    title: 'Portofolio Old',
    teks:
      'Project website pertama yang terdiri dari Skills dan beberapa project lama pada website tersebut',
    img: '/img/newPortofolio.png',
    stylingklik: 'btn btn-outline btn-primary sm:btn-sm md:btn-md lg:btn-lg xl:btn-xl lg:mx-64 lg:my-32',
    kalimatButton: 'Click Here',
    link: 'https://www.google.com/',
  },
  {
    id: 2,
    title: 'Ucapan Hari Raya Idul Fitri',
    teks:
      'Sebuah Project yang dibuat untuk mengucapkan Selamat Hari Raya Idul Fitri, pada website tersebut terdapat beberapa fitur button yang langsung mengarah ke dana kaget, user yang mengakses nya mendapatkan gift THR dari website ini',
    img: '/img/idulFitri.png',
    stylingklik: 'btn btn-outline btn-primary sm:btn-sm md:btn-md lg:btn-lg xl:btn-xl  lg:mx-64 lg:my-10',
    kalimatButton: 'Click Here',
    link: 'https://www.google.com/',
  },
  {
    id: 3,
    title: 'Website Film',
    teks:
      'Website film random dengan menggunakan API free film, beberapa fitur masih coming soon yang nantinya update lagi',
    img: '/img/MoviesWeb.png',
    stylingklik: 'btn btn-outline btn-primary sm:btn-sm md:btn-md lg:btn-lg xl:btn-xl  lg:mx-64 lg:my-10',
    kalimatButton: 'Click here',
    link: 'https://www.google.com/',
  },
  {
    id: 4,
    title: 'Auto Random Color',
    teks:
      'Project random dengan melihat warna warni pada box yang sudah disediakan',
    img: '/img/randomColor.png',
    stylingklik: 'btn btn-outline btn-primary sm:btn-sm md:btn-md lg:btn-lg xl:btn-xl  lg:mx-64 lg:my-16',
    kalimatButton: 'Click Here',
    link: 'https://www.google.com/',
  },
])
</script>

<template>
  <div data-aos="fade-up" class="container mx-auto px-4 py-8 sm:px-6 lg:px-8" id="project">
    <Heading
      level = '1'
      text="Project"
      Styling="text-center text-xl capitalize mb-10 sm:text-2xl md:text-4xl lg:text-6xl"
    />

    <div class="grid grid-cols-1 gap-6 sm:grid-cols-2 md:grid-cols-2">
      <Card
        v-for="card in cards"
        :key="card.id"
        :Title="card.title"
        :Teks="card.teks"
        :Imgsrc="card.img"
        styleImage="w-3/4 mx-auto rounded-xl"
        styleHeading="font-bold text-xl mx-15 mb-5 text-center"
        :StyleKalimat="'mt-5 mx-0 text-lg sm:mx-20 text-xl md:text-2xl'"
        :styleButton="card.stylingklik"
        :textbutton="card.kalimatButton"
        :Link="card.link"
      />
    </div>

    <!-- Optional: Certificate Button -->
    <div class="flex justify-center mt-16">
      <a
        href="#sertifikasi"
        class="btn btn-primary text-white text-lg sm:text-xl md:text-2xl"
      >
        View Certificates
      </a>
    </div>
  </div>
</template>
