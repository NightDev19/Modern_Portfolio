<template>
  <div
    class="navbar fixed top-0 z-30 h-16 lg:h-14 w-full bg-base-600 bg-opacity-40 shadow-xl backdrop-blur-lg border border-opacity-20 border-gray-700"
  >
    <div class="navbar-start">
      <div class="dropdown">
        <div tabindex="0" role="button" class="btn btn-ghost btn-circle">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-5 w-5"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16M4 18h7"
            />
          </svg>
        </div>
        <ul
          tabindex="0"
          class="menu menu-sm dropdown-content mt-3 z-[1] p-2 shadow bg-base-100 rounded-box w-52"
        >
          <li><a href="#home">Home</a></li>
          <li><a href="#about">About</a></li>
          <li><a href="#skills">Skills</a></li>
          <li><a href="#education">Education</a></li>
          <li><a href="#experience">Experience</a></li>
          <li><a href="#projects">Projects</a></li>
          <li><a href="#contacts">Contacts</a></li>
        </ul>
      </div>
    </div>
    <div class="navbar-center">
      <a href="/" class="btn btn-ghost text-sm lg:text-xl">&lt;NightDev/&gt;</a>
    </div>
    <div class="navbar-end flex gap-2 pr-2">
      <div class="tooltip tooltip-bottom" data-tip="Github">
        <a href=""
          ><Icon icon="fontisto:github" class="lg:w-6 lg:h-6 w-4 h-4"
        /></a>
      </div>
      <div class="tooltip tooltip-bottom" data-tip="Facebook">
        <a href=""
          ><Icon icon="fontisto:facebook" class="lg:w-6 lg:h-6 w-4 h-4"
        /></a>
      </div>

      <div class="tooltip tooltip-bottom" data-tip="Insta">
        <a href=""
          ><Icon icon="fontisto:instagram" class="lg:w-6 lg:h-6 w-4 h-4"
        /></a>
      </div>
    </div>
  </div>
</template>

<script>
import { Icon } from "@iconify/vue";

export default {
  name: "Navbar",
  components: {
    Icon,
  },
};
</script>
