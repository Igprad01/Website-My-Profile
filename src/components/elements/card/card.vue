<script setup>
// import Heading from '../Heading/Heading.vue'
// import Kalimat from '../Kalimat/Paragraph.vue'
// import Image from '../../image/Image.vue'

defineProps({
  Teks: String,
  Title: String,
  styleHeading: String,
  Imgsrc: String,
  Ket: String,
  styleImage: String,
  StyleKalimat: String,
  styleButton: String,
  textbutton: String,
  Link: String
})
</script>

<template>
  <div class="border box-border px-3 py-3 bg-transparent">
    <div class="mx-auto">
      <Heading :Text="Title" :level = "1" :Styling="styleHeading" />
      <Image :src="Imgsrc" :alt="Ket" :styleImg="styleImage" />
      <Kalimat :teks="Teks" :Styling="StyleKalimat" />
      <a :href="Link">
        <button :class="styleButton">
          {{ textbutton }}
        </button>
      </a>
    </div>
  </div>
</template>
