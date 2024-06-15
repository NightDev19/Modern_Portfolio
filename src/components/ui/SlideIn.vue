<template>
  <div class="slide-in" ref="slideInElement">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "SlideIn",
  mounted() {
    this.observer = new IntersectionObserver(
      (entries) => {
        if (entries[0].isIntersecting) {
          this.startAnimation();
          this.observer.disconnect(); // Stop observing once animation is triggered
        }
      },
      { threshold: 0.5 } // Trigger when 50% of the element is visible
    );

    // Check if element is already in view
    const initialIntersection = this.observer
      .takeRecords()
      .some((entry) => entry.isIntersecting);

    if (initialIntersection) {
      this.startAnimation();
      this.observer.disconnect(); // Stop observing if element is already in view
    } else {
      this.observer.observe(this.$refs.slideInElement);
    }
  },
  methods: {
    startAnimation() {
      this.$refs.slideInElement.classList.add("start-animation");
    },
  },
};
</script>

<style>
.slide-in {
  visibility: hidden;
}

.start-animation {
  animation: slideIn 0.5s forwards;
  visibility: visible;
}

@keyframes slideIn {
  from {
    transform: translateX(-100%);
  }
  to {
    transform: translateX(0);
  }
}
</style>
