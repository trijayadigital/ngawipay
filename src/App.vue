<script setup></script>

<template>
  <section
    class="h-screen w-screen flex items-center justify-center bg-gradient-to-br from-white to-blue-100 overflow-hidden relative"
  >
    <div
      class="flex z-20 flex-col md:flex-row items-center w-full max-w-6xl relative overflow-hidden px-10"
    >
      <div class="flex-1">
        <div class="flex justify-center md:justify-start items-center mb-14">
          <img src="@/assets/logo_long.png" alt="wrapper" class="w-[22rem]" />
        </div>
        <h1
          class="text-5xl md:text-7xl text-center md:text-left font-bold text-gray-900 mb-8 md:mb-16 leading-tight"
        >
          Coming Soon
        </h1>
        <p
          class="text-lg text-slate-600 max-w-xl text-center md:text-left mb-10"
        >
          Ada yang diam-diam bergerak di Ngawi, tunggu saja...
        </p>
      </div>
      <div
        class="flex-1 flex justify-center mt-12 md:mt-0 relative size-[20rem] md:size-[25rem]"
      >
        <div class="absolute inset-0 flex items-center justify-center pb-10">
          <img
            src="@/assets/logo.png"
            alt="wrapper"
            class="w-[12rem] md:w-[14rem]"
          />
        </div>
        <img
          src="@/assets/logo_wrapper.png"
          alt="wrapper"
          class="size-[20rem] md:size-[25rem]"
        />
      </div>
    </div>
    <div
      class="absolute z-10 -left-80 size-[64rem] rounded-full bg-blue-100/80 blur-3xl"
    ></div>
  </section>
</template>

<style></style>
