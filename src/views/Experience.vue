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
                <br />S.Y. 2023 - current
            </TimelineItem>
            <TimelineItem title="Internship">
                Worked as an intern in the field of IT Support and Encoder at
                South East Star Enterprises .
                <br />S.Y March 2024 - May 2024
            </TimelineItem>
            <TimelineItem title="Secondary Teacher">
                Worked as an Teacher in the field of ICT - Computer programming
                at Tanauan City Academy ,
                <br />S.Y. August 2024 - 2025
            </TimelineItem>
            <TimelineItem title="Front End Developer">
                Worked as a Front End Developer at Innocore Solutions.
                <br />S.Y. August 2024 - 2025
            </TimelineItem>
            <TimelineItem title="Software Engineer III">
                Worked as a Software Engineer III at CodeFusion IT Solutions
                Company.
                <br />S.Y. August 2025 - current
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
