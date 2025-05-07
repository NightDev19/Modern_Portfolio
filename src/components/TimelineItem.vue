<template>
  <!-- Main container with vertical line and padding -->
  <div class="flex flex-row items-start py-3" :class="['custom-border', className]">
    <!-- Slide-in animation wrapper -->
    <SlideIn>
      <div class="w-full rounded-md mx-5">
        <!-- Section title -->
        <h1 class="text-white text-2xl font-bold">{{ title }}</h1>

        <!-- Content passed from parent using slot -->
        <p class="text-gray-400 mt-1 pb-2">
          <slot></slot>
        </p>
      </div>
    </SlideIn>
  </div>
</template>

<script>
import SlideIn from './ui/SlideIn.vue'; // Import animation component

export default {
  name: 'SectionCard', // Helpful name for devtools

  props: {
    // Title to display at the top
    title: {
      type: String,
      required: true,
    },
    // Optional additional CSS classes for customization
    className: {
      type: String,
      default: '',
    },
  },

  components: {
    SlideIn, // Register slide animation component
  },
};
</script>

<style scoped>
/* Custom left border style (5px wide, colored) */
.custom-border {
  border-left: 5px solid #62778d;
}
</style>
