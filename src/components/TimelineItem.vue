<template>
  <div
    class="flex flex-row items-start border-l-5 border-gray-800 py-3"
    :class="className"
  >
    <SlideIn>
      <div class="w-full rounded-md mx-5">
        <h1 class="text-white text-2xl font-bold">{{ title }}</h1>
        <p class="text-gray-400 mt-1 pb-2"><slot></slot></p>
      </div>
    </SlideIn>
  </div>
</template>

<script>
import SlideIn from "./ui/SlideIn.vue"; // Import the SlideIn component

export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    className: {
      type: String,
      default: "",
    },
  },
  components: {
    SlideIn, // Register the SlideIn component
  },
};
</script>

<style scoped>
.border-l-5 {
  border-left-width: 5px;
  border-left-color: #62778d; /* Choose your desired color */
}
</style>
