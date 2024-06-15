<template>
  <SlideIn>
    <div
      class="bg-gray-900 w-full h-full rounded-lg shadow-md overflow-hidden border-t-4 border-sky-400"
    >
      <img
        :src="image"
        :alt="title"
        class="w-full h-48 object-cover object-center p-2 rounded-lg"
      />
      <div class="p-4">
        <div class="flex justify-between items-center">
          <h2 class="font-bold text-xl text-white truncate">{{ title }}</h2>
          <div class="flex space-x-4">
            <div class="tooltip tooltip-top" data-tip="Live Site">
              <a :href="link" target="_blank" rel="noopener noreferrer">
                <Icon
                  icon="mdi:link"
                  class="lg:w-6 lg:h-6 w-4 h-4 text-blue-400 hover:text-blue-600"
                />
              </a>
            </div>
            <div class="tooltip tooltip-top" data-tip="Github">
              <a :href="repo" target="_blank" rel="noopener noreferrer">
                <Icon
                  icon="fontisto:github"
                  class="lg:w-6 lg:h-6 w-4 h-4 text-blue-400 hover:text-blue-600"
                />
              </a>
            </div>
          </div>
        </div>
        <p class="text-gray-400 mt-2">
          {{ truncatedDescription }}
          <span
            v-if="description.length > maxDescriptionLength"
            class="text-blue-400 cursor-pointer hover:text-blue-600"
            @click="toggleDescription"
          >
            {{ isExpanded ? "See less" : "See more" }}
          </span>
        </p>
        <div class="flex items-center mt-4 space-x-2">
          <Icon
            v-for="lang in langs"
            :key="lang"
            :icon="lang"
            class="w-8 h-8"
          />
        </div>
      </div>
    </div>
  </SlideIn>
</template>

<script>
import { Icon } from "@iconify/vue";
import SlideIn from "./ui/SlideIn.vue";

export default {
  name: "ProjectCard",

  props: {
    title: String,
    description: String,
    link: String,
    repo: String,
    image: String,
    langs: Array,
  },

  data() {
    return {
      isExpanded: false,
      maxDescriptionLength: 50, // Set maximum length for the description truncation
    };
  },

  computed: {
    truncatedDescription() {
      if (
        this.isExpanded ||
        this.description.length <= this.maxDescriptionLength
      ) {
        return this.description;
      }
      return this.description.slice(0, this.maxDescriptionLength) + "...";
    },
  },

  methods: {
    toggleDescription() {
      this.isExpanded = !this.isExpanded;
    },
  },

  components: {
    Icon,
    SlideIn,
  },
};
</script>

<style scoped>
.bg-gray-900 {
  background-color: #1f2937;
}

.text-gray-400 {
  color: #9ca3af;
}

.text-blue-400 {
  color: #60a5fa;
}

.text-blue-400:hover {
  color: #3b82f6;
}

.shadow-md {
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.truncate {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
</style>
