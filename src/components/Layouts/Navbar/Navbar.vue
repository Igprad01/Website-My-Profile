<script setup>
import { ref } from 'vue'
import NavbarList from '../../Elements/NavbarList/NavbarList.vue'

const Open = ref(false)

const hamburger = () => {
  Open.value = !Open.value
}
</script>

<template>
  <nav class="sticky top-10 z-50 flex justify-center items-center text-black my-12 text-2xl">
    <!-- Desktop Navbar -->
    <div class="hidden md:flex bg-gray-300 rounded-full shadow-lg px-10 py-5 pl-28 cursor-pointer hover:shadow-black delay-75">
      <NavbarList />
    </div>

    <!-- Mobile Hamburger -->
    <div class="md:hidden flex justify-end items-end w-full pr-6">
      <button @click="hamburger">
        <svg viewBox="0 0 100 80" width="20" height="20">
          <rect width="100" height="20" fill="white" />
          <rect y="30" width="100" height="20" fill="white" />
          <rect y="60" width="100" height="20" fill="white" />
        </svg>
      </button>
    </div>

    <!-- Mobile Menu -->
    <div
      v-if="Open"
      class="absolute top-20 right-10 left-5 overflow-visible bg-white px-5 py-5 items-center rounded-lg md:hidden z-10"
    >
      <NavbarList styling="flex flex-col justify-start space-y-3 text-lg sm:text-xl" />
    </div>

    <!-- Optional Toggle Button -->
    <!--
    <div class="absolute right-32">
      <Toggle />
    </div>
    -->
  </nav>
</template>
