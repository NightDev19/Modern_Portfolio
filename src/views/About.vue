<template>
  <section
    class="pb-5 w-full bg-gray-950"
    id="about"
    style="padding-top: 5rem; margin-top: -5rem"
  >
    <header class="mx-6 pt-6 md:mx-10">
      <h1 class="text-white font-bold text-3xl md:text-5xl">
        About Me
        <b
          class="text-transparent bg-clip-text bg-gradient-to-r from-sky-200 to-blue-400"
        >
          .
        </b>
      </h1>
      <div
        class="h-1 w-24 rounded-full bg-gradient-to-r from-sky-200 to-blue-400 md:w-32 md:h-2"></div>
    </header>

    <div class="flex flex-wrap justify-start mx-6 md:mx-10 mt-5">
      <SlideIn v-for="(item, index) in info" :key="index">
        <div class="text-white text-lg leading-relaxed">
          <h2 class="text-2xl font-semibold">{{ item.name }}</h2>
          <p class="mt-2">{{ item.description }}</p>
        </div>
      </SlideIn>
    </div>
  </section>
</template>

<script>
import info from "../data/aboutme.json";
import SlideIn from "../components/ui/SlideIn.vue";

export default {
  components: {
    SlideIn,
  },
  data() {
    return {
      info,
    };
  },
};
</script>
