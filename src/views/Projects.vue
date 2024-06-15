<template>
  <section
    class="pb-5 w-full bg-gray-950"
    id="projects"
    style="padding-top: 5rem; margin-top: -5rem"
  >
    <header class="mx-6 pt-6 md:mx-10">
      <h1 class="text-white font-bold text-3xl md:text-5xl">
        Projects
        <b
          class="text-transparent bg-clip-text bg-gradient-to-r from-sky-200 to-blue-400 "
        >
          .
        </b>
      </h1>
      <div
        class="h-1 w-14 rounded-full bg-gradient-to-r from-sky-200 to-blue-400 md:w-20 md:h-2 mt-4"
      ></div>
    </header>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mx-1 p-8 md:mx-10">
      <ProjectCard
        v-for="project in projects"
        :key="project.id"
        :title="project.title"
        :description="project.description"
        :link="project.link"
        :repo="project.repo"
        :image="project.image"
        :langs="project.langs"
      />
    </div>
  </section>
</template>

<script>
import ProjectCard from "../components/ProjectCard.vue";
import projectsData from "../data/projects.json";

export default {
  components: {
    ProjectCard,
  },
  data() {
    return {
      projects: projectsData,
    };
  },
};
</script>

<style>
/* Add your custom styles here */
</style>
