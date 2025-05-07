<template>
  <nav
    class="fixed top-0 w-full bg-gray-900 bg-opacity-70 backdrop-blur-md shadow-md border-b border-gray-700 z-30"
  >
    <div class="flex items-center justify-between h-16 px-4">
      <!-- Dropdown Menu -->
      <div class="relative">
        <button @click="showMenu = !showMenu" class="btn btn-ghost text-white">
          <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16M4 18h7"
            />
          </svg>
        </button>
        <ul v-show="showMenu" class="absolute bg-gray-800 text-white mt-2 rounded shadow w-48">
          <li v-for="item in menuItems" :key="item.href">
            <a
              :href="item.href"
              @click="showMenu = false"
              class="block px-4 py-2 hover:bg-gray-700"
              >{{ item.text }}</a
            >
          </li>
        </ul>
      </div>

      <!-- Logo -->
      <a href="/" class="text-white text-lg font-bold">&lt;NightDev/&gt;</a>

      <!-- Social Links -->
      <div class="flex gap-3">
        <a
          v-for="icon in icons"
          :key="icon.name"
          :href="icon.link"
          target="_blank"
          class="text-white hover:text-sky-400"
        >
          <Icon :icon="icon.name" class="w-5 h-5" />
        </a>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue';
import { Icon } from '@iconify/vue';

const showMenu = ref(false);

const menuItems = [
  { text: 'Home', href: '#home' },
  { text: 'About', href: '#about' },
  { text: 'Skills', href: '#skills' },
  { text: 'Education', href: '#education' },
  { text: 'Experience', href: '#experience' },
  { text: 'Projects', href: '#projects' },
  { text: 'Contacts', href: '#contacts' },
];

const icons = [
  { name: 'fontisto:github', link: 'https://github.com/NightDev19' },
  { name: 'fontisto:facebook', link: 'https://www.facebook.com/tajan.sherwinjefferson/' },
  {
    name: 'fontisto:linkedin',
    link: 'https://www.linkedin.com/in/sherwin-jefferson-tajan-4b3199269/',
  },
];
</script>
