<template>
  <nav class="bg-gray-800 p-4">
    <div class="container mx-auto flex justify-between items-center">
      <div class="text-white text-xl font-bold">
        <RouterLink to="/"> MyApp </RouterLink>
      </div>
      <div class="hidden md:flex space-x-4">
        <RouterLink to="/" class="text-gray-300 hover:text-white">Home</RouterLink>
        <RouterLink to="/signin" class="text-gray-300 hover:text-white">Sign In</RouterLink>
        <RouterLink to="/signup" class="text-gray-300 hover:text-white">Sign Up</RouterLink>
      </div>
      <div class="md:hidden">
        <button @click="toggleMenu" class="text-white focus:outline-none">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16m-7 6h7"
            />
          </svg>
        </button>
      </div>
    </div>

    <div v-if="isMenuOpen" class="md:hidden mt-4">
      <router-link to="/" class="block text-gray-300 hover:text-white py-2">Home</router-link>
      <router-link to="/signin" class="block text-gray-300 hover:text-white py-2"
        >Sign In</router-link
      >
      <router-link to="/signup" class="block text-gray-300 hover:text-white py-2"
        >Sign Up</router-link
      >
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'
import { RouterLink } from 'vue-router'

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}
</script>
