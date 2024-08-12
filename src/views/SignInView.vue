<template>
  <div class="min-h-screen bg-gray-900 text-white flex flex-col items-center justify-center">
    <h1 class="text-3xl font-bold mb-6">Sign In</h1>
    <form class="w-full max-w-sm">
      <div class="mb-4">
        <input
          class="w-full p-2 bg-gray-800 text-white border border-gray-700 rounded"
          type="text"
          placeholder="Email"
        />
      </div>
      <div class="mb-4">
        <input
          class="w-full p-2 bg-gray-800 text-white border border-gray-700 rounded"
          type="password"
          placeholder="Password"
        />
      </div>
      <button class="w-full p-2 bg-blue-600 rounded hover:bg-blue-700">Sign In</button>
    </form>
  </div>
</template>

<script setup lang="ts">
// Nenhuma lógica adicional necessária para esta view
</script>
