<template>
  <section
    class="pb-5 w-full bg-gray-950"
    id="experience"
    style="padding-top: 5rem; margin-top: -5rem"
  >
    <header class="mx-6 pt-6 md:mx-10">
      <h1 class="text-white font-bold text-3xl md:text-5xl">
        Experience
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
    <div class="mx-6 pt-8 md:mx-10">
      <TimelineItem title="Freelancing">
        One year freelancing as a web developer, navigating projects and
        relishing the freedom of self-employment.
      </TimelineItem>
      <TimelineItem title="Internship">
        Worked as an intern in the field of IT Support and Encoder at South East
        Star Enterprises .
      </TimelineItem>
    </div>
  </section>
</template>

<script>
import TimelineItem from "../components/TimelineItem.vue";

export default {
  components: {
    TimelineItem,
  },
};
</script>
<style scoped>
#experience {
  scroll-padding-top: 5rem;
}
</style>
