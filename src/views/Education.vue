<template>
  <section
    class="pb-5 w-full bg-gray-950"
    id="education"
    style="padding-top: 5rem; margin-top: -5rem"
  >
    <header class="mx-6 pt-6 md:mx-10">
      <h1 class="text-white font-bold text-3xl md:text-5xl">
        Education
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
    <SlideIn>
      <div class="mx-6 pt-8 md:mx-10">
        <TimelineItem title="Junior High School">
          Studied Grade 7-10 at Wawa National High School (2013 to 2018)
        </TimelineItem>
        <TimelineItem title="Senior High School">
          Studied Grade 11 to 12 at Nova Schola Tanauan NST (2018 to 2020)
        </TimelineItem>
        <TimelineItem title="College">
          Studied Bachelor of Science in Information Technology at Batangas
          State University - JPLPC (2020 - 2024)
        </TimelineItem>
      </div>
    </SlideIn>
  </section>
</template>

<script>
import TimelineItem from "../components/TimelineItem.vue";
import SlideIn from "../components/ui/SlideIn.vue";
export default {
  components: {
    TimelineItem,
    SlideIn,
  },
};
</script>
