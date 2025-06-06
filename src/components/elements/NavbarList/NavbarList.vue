<script setup>
defineProps({
  styling: String
})

// Daftar menu navbar
const List = [
  { name: 'Home', link: '#home' },
  { name: 'About', link: '#about' },
  { name: 'Project', link: '#project' },
  { name: 'Certification', link: '#sertifikasi' }
]
</script>

<template>
  <ul :class="`mr-10 ${styling}`">
    <li 
      v-for="(item, index) in List" 
      :key="index" 
      class="inline-block mr-10"
    >
      <a 
        :href="item.link" 
        class="hover:text-white delay-100 capitalize"
      >
        {{ item.name }}
      </a>
    </li>
  </ul>
</template>
