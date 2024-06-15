<template>
    <section class="h-screen bg-gray-950 flex items-center justify-center" id="home">
      <div class="text-center w-full">
        <!-- Greeting Section -->
        <div class="w-full flex justify-center items-center mt-10 mb-5">
          <div class="text-white text-center py-1.5 px-4 font-mono text-sm bg-gray-900 rounded-full md:py-2 md:px-6 md:text-xl">
            Kumusta? <span class="inline-block animate-wave">👋</span>, I'm Sherwin Tajan
          </div>
        </div>
  
        <!-- Experience Description -->
        <h1 class="scroll-m-20 text-3xl font-extrabold tracking-tight md:text-7xl text-white mt-1 md:mx-20">
          Experienced
          <b class="text-transparent bg-clip-text bg-gradient-to-r from-sky-200 to-blue-400">
            full-stack web developer
          </b>
          with a focus on
          <b class="text-transparent bg-clip-text bg-gradient-to-r from-sky-200 to-blue-400">
            front-end development
          </b>
          .
        </h1>
  
        <!-- Statistics Section -->
        <div class="flex justify-center items-center mt-5">
          <ul class="gap-3 flex justify-between items-center sm:gap-12 text-white w-[calc(100vw-5rem)] sm:w-fit">
            <li class="flex flex-col sm:flex-row items-center gap-1 lg:gap-2">
              <span class="flex items-center font-bold bg-[#0001] py-1 px-3 rounded-xl">+3</span>
              <span class="text-[0.71rem] sm:text-[0.81rem] leading-[1] text-center sm:text-left">
                Years of<br />experience
              </span>
            </li>
            <span class="h-8 border-r-[1px] border-dashed border-light-gray-secondary"></span>
            <li class="flex flex-col sm:flex-row items-center gap-1 lg:gap-2">
              <span class="flex items-center font-bold bg-[#0001] py-1 px-3 rounded-xl">100k</span>
              <span class="text-[0.71rem] sm:text-[0.81rem] leading-[1] text-center sm:text-left">
                Lines of<br />code written
              </span>
            </li>
            <span class="h-8 border-r-[1px] border-dashed border-light-gray-secondary"></span>
            <li class="flex flex-col sm:flex-row items-center gap-1 lg:gap-2">
              <span class="flex items-center font-bold bg-[#0001] py-1 px-3 rounded-xl">5k</span>
              <span class="text-[0.71rem] sm:text-[0.81rem] leading-[1] text-center sm:text-left">
                Cups of coffee<br />consumed
              </span>
            </li>
          </ul>
        </div>
  
        <!-- Buttons -->
        <div class="text-center w-full mt-7 md:mt-10 flex justify-center">
          <button
            @click="downloadResume"
            class="flex items-center justify-center px-5 py-2 w-[160px] bg-white text-gray-900 text-sm lg:text-md rounded-full mx-3 font-mono hover:bg-white hover:opacity-90 md:scale-150 md:mx-14"
          >
            <Icon icon="mdi:download" class="mr-1 h-4 w-4" />
            Download CV
          </button>
          <button
            @click="contact"
            class="flex items-center justify-center px-5 py-2 w-[160px] bg-gray-900 text-white text-sm lg:text-md rounded-full mx-3 font-mono md:scale-150 md:mx-14"
          >
            <Icon icon="mdi:chat" class="mr-1 h-4 w-4" />
            Contact
          </button>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  import { Icon } from "@iconify/vue";
  
  export default {
    name: "Home",
    components: {
      Icon,
    },
    methods: {
      downloadResume() {
        window.location.href = "https://example.com/Sherwin_Tajan_Developer_Resume.pdf";
      },
      contact() {
        window.location.href = "#contacts";
      },
    },
  };
  </script>
  
  <style scoped>
  .animate-wave {
    animation: wave-animation 2s infinite;
  }
  
  @keyframes wave-animation {
    0%, 100% { transform: rotate(0deg); }
    50% { transform: rotate(25deg); }
  }
  </style>
  