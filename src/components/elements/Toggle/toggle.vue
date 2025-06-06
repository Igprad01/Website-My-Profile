<script setup>
import { ref } from 'vue'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { faSun, faMoon } from '@fortawesome/free-solid-svg-icons'

// State: dark mode
const isDarkMode = ref(false)

const handle = () => {
  isDarkMode.value = !isDarkMode.value
}
</script>

<template>
  <button 
    class="btn btn-square bg-white hover:bg-white"
    @click="handle"
  >
    <FontAwesomeIcon :icon="isDarkMode ? faMoon : faSun" size="lg" />
  </button>
</template>

<script>
export default {
  components: {
    FontAwesomeIcon
  }
}
</script>
