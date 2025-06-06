<script setup>
import { onMounted, ref } from 'vue'
// import AOS from 'aos'
// import 'aos/dist/aos.css'

import Card from '@/components/Elements/Card/Card.vue'
import Heading1 from '@/components/Elements/Heading/Heading.vue'

// onMounted(() => {
//   AOS.init({ duration: 2000 })
// })

const kartu = ref([
  {
    id: 1,
    judul: 'Data Analysis',
    kalimat: 'Sertifikasi Penyelesaian Course FreeCodeCamp Data Analysis With Python',
    buttonstyle: 'btn btn-outline btn-primary sm:btn-sm md:btn-md lg:btn-lg xl:btn-xl mt-5',
    kalimatButton: 'Click Here',
  },
  {
    id: 2,
    judul: 'Data Analysis - Python Introduction',
    kalimat: 'Sertifikasi Penyelesaian Course Data Analysis With Python DQLab Free Class',
    buttonstyle: 'btn btn-outline btn-primary sm:btn-sm md:btn-md lg:btn-lg xl:btn-xl mt-5',
    kalimatButton: 'Click Here',
  },
  {
    id: 3,
    judul: 'SQL Fundamental for Data Science',
    kalimat: 'Sertifikasi penyelesaian Course SQL DQLab Free Class',
    buttonstyle: 'btn btn-outline btn-primary sm:btn-sm md:btn-md lg:btn-lg xl:btn-xl mt-5',
    kalimatButton: 'Click Here',
  },
  {
    id: 4,
    judul: 'Microsoft Excel Pivot Table',
    kalimat: 'Sertifikasi Penyelesaian Course Excel pivot Table Myskill Id',
    buttonstyle: 'btn btn-outline btn-primary sm:btn-sm md:btn-md lg:btn-lg xl:btn-xl mt-5',
    kalimatButton: 'Click Here',
  },
])
</script>

<template>
  <div
    data-aos="fade-up"
    class="container mx-auto px-4 py-8 sm:px-6 lg:px-8"
    id="sertifikasi"
  >
    <Heading
      level = '1'
      Text="Certification"
      Styling="text-center text-xl mb-10 capitalize sm:text-2xl md:text-4xl lg:text-6xl"
    />

    <div class="grid grid-cols-1 gap-7">
      <Card
        v-for="item in kartu"
        :key="item.id"
        :Title="item.judul"
        :Teks="item.kalimat"
        styleHeading="text-3xl"
        StyleKalimat="text-2xl"
        :styleButton="item.buttonstyle"
        :textbutton="item.kalimatButton"
      />
    </div>
  </div>
</template>
