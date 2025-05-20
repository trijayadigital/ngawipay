<script setup>
import { onMounted, ref } from 'vue';

const audioPlayer = ref(null);
const isPlaying = ref(false);

const toggleAudio = () => {
  if (!audioPlayer.value) {
    audioPlayer.value = new Audio('/kartonyono_medot_janji.mp3');
    audioPlayer.value.loop = true;

    // Tambahkan event listeners sekali saja
    audioPlayer.value.addEventListener('play', () => {
      isPlaying.value = true;
    });

    audioPlayer.value.addEventListener('pause', () => {
      isPlaying.value = false;
    });
  }

  if (isPlaying.value) {
    audioPlayer.value.pause();
  } else {
    audioPlayer.value.play();
  }
};

// Cleanup pada saat component unmount
onMounted(() => {
  return () => {
    if (audioPlayer.value) {
      audioPlayer.value.pause();
      audioPlayer.value = null;
    }
  };
});
</script>

<template>
  <section class="h-screen w-screen flex items-center justify-center bg-gradient-to-br from-white to-blue-100 overflow-hidden relative">
    <div class="flex z-20 flex-col md:flex-row items-center w-full max-w-6xl relative overflow-hidden px-10">
      <div class="flex-1">
        <div class="flex justify-center md:justify-start items-center mb-14">
          <img src="@/assets/logo_long.png" alt="wrapper" class="w-[22rem]" />
        </div>
        <h1
          class="text-6xl md:text-7xl text-center md:text-left font-bold bg-gradient-to-r from-[#0096FF] to-[#49c1ee] text-transparent bg-clip-text mb-2 sm:mb-4 md:mb-12 leading-tight md:h-[6rem] sm:h-[7rem] h-[9rem] xs:h-[10rem]"
        >
          Coming Soon
        </h1>
        <p class="text-lg text-slate-600 max-w-xl text-center md:text-left mb-10">Ada yang diam-diam bergerak di Ngawi, tunggu saja...</p>
      </div>
      <div class="flex-1 flex justify-center mt-12 md:mt-0 relative size-[20rem] md:size-[25rem]">
        <div class="absolute z-10 w-full h-full flex items-center justify-center">
          <button @click="toggleAudio" class="bg-white/80 hover:bg-white rounded-full p-3 shadow-lg transition-all duration-300 hover:scale-110 mb-5">
            <svg v-if="isPlaying" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="size-16 text-blue-500">
              <path
                d="M6.75 4.75a.75.75 0 00-.75.75v13a.75.75 0 00.75.75h2.5a.75.75 0 00.75-.75v-13a.75.75 0 00-.75-.75h-2.5zm8 0a.75.75 0 00-.75.75v13a.75.75 0 00.75.75h2.5a.75.75 0 00.75-.75v-13a.75.75 0 00-.75-.75h-2.5z"
              />
            </svg>
            <svg v-else xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="size-16 text-blue-500">
              <path
                fill-rule="evenodd"
                d="M4.5 5.653c0-1.427 1.529-2.33 2.779-1.643l11.54 6.347c1.295.712 1.295 2.573 0 3.286L7.28 19.99c-1.25.687-2.779-.217-2.779-1.643V5.653z"
                clip-rule="evenodd"
              />
            </svg>
          </button>
        </div>
        <div class="absolute inset-0 flex items-center justify-center pb-10">
          <img src="@/assets/logo.png" alt="wrapper" class="w-[12rem] md:w-[14rem]" />
        </div>
        <img src="@/assets/logo_wrapper.png" alt="wrapper" class="size-[20rem] md:size-[25rem]" />
      </div>
    </div>
    <div class="absolute z-10 -left-80 size-[64rem] rounded-full bg-blue-200/80 blur-3xl"></div>
  </section>
</template>

<style></style>
