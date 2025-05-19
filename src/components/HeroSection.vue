<template>
  <section
    class="min-h-screen flex items-center justify-center bg-gradient-to-br from-white to-blue-50 rounded-3xl shadow-xl p-8"
  >
    <div class="flex flex-col md:flex-row items-center w-full max-w-6xl">
      <!-- Kiri: Teks -->
      <div class="flex-1">
        <div class="flex items-center mb-8">
          <div class="flex items-center space-x-2">
            <div class="flex items-center space-x-1">
              <span class="w-2.5 h-2.5 bg-blue-500 rounded-full"></span>
              <span class="w-2.5 h-2.5 bg-blue-500 rounded-full"></span>
              <span class="w-2.5 h-2.5 bg-blue-500 rounded-full"></span>
            </div>
            <span class="font-bold text-2xl text-gray-800">brix</span>
            <span
              class="bg-blue-100 text-blue-600 font-bold px-2 py-0.5 rounded-md text-sm"
              >AI</span
            >
          </div>
        </div>
        <h1
          class="text-5xl md:text-6xl font-bold text-gray-900 mb-6 leading-tight"
        >
          A bold step<br />
          toward AI-driven<br />
          communication
        </h1>
        <p class="text-lg text-gray-500 max-w-xl">
          We are revolutionizing AI interactions by providing businesses with
          intuitive, scalable, and intelligent solutions designed for real-world
          impact.
        </p>
      </div>
      <!-- Kanan: Logo -->
      <div class="flex-1 flex justify-center mt-12 md:mt-0">
        <div
          class="bg-white rounded-full shadow-lg p-12 flex items-center justify-center relative"
          style="width: 320px; height: 320px"
        >
          <!-- Logo brix AI -->
          <div
            class="absolute left-1/2 top-1/2 -translate-x-1/2 -translate-y-1/2 flex flex-col items-center space-y-2"
          >
            <div class="flex justify-center">
              <span class="w-10 h-10 bg-blue-500 rounded-full"></span>
            </div>
            <div class="flex space-x-4">
              <span class="w-10 h-10 bg-blue-500 rounded-full"></span>
              <span class="w-10 h-10 bg-blue-500 rounded-full"></span>
            </div>
            <div class="flex space-x-4">
              <span class="w-10 h-10 bg-blue-500 rounded-full"></span>
              <span class="w-10 h-10 bg-blue-500 rounded-full"></span>
              <span class="w-10 h-10 bg-blue-500 rounded-full"></span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// Tidak perlu script khusus
</script>
