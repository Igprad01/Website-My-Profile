<script setup>
defineProps({
  teks: String,
  Styling: String
})
</script>

<template>
  <p :class="Styling">{{ teks }}</p>
</template>
