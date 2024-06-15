<template>
  <section class="pb-5 w-full bg-gray-950" id="skills" style="padding-top: 5rem; margin-top: -5rem;">
    <header class="mx-6 pt-6 md:mx-10">
      <h1 class="text-white font-bold text-3xl md:text-5xl">
        Skills
        <b
          class="text-transparent bg-clip-text bg-gradient-to-r from-sky-200 to-blue-400"
        >
          .
        </b>
      </h1>
      <div
        class="h-1 w-14 rounded-full bg-gradient-to-r from-sky-200 to-blue-400 md:w-20 md:h-2"
      ></div>
    </header>

    <div class="flex flex-wrap justify-start mx-6 md:mx-10 mt-5">
      <SlideIn>
        <div
          v-for="skill in skills"
          :key="skill.name"
          class="tooltip"
          :data-tip="skill.name"
        >
          <div
            class="py-4 px-4 bg-gray-900 rounded-xl mx-1.5 my-1.5 md:my-2 md:mx-2 text-white"
          >
            <Icon
              :icon="skill.icon"
              class="text-white h-10 w-10 md:h-16 md:w-16"
            />
          </div>
        </div>
      </SlideIn>
    </div>
  </section>
</template>

<script>
import { Icon } from "@iconify/vue";
import skills from "../data/skills.json";
import SlideIn from "../components/ui/SlideIn.vue";

export default {
  components: {
    Icon,
    SlideIn,
  },
  data() {
    return {
      skills,
    };
  },
};
</script>
