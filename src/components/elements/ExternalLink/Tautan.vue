<script setup>
defineProps({
  href: String,
  konten: String,
  styling: String
})
</script>

<template>
  <a :href="href" :class="styling" target="_blank" rel="noopener noreferrer">
    {{ konten }}
  </a>
</template>
