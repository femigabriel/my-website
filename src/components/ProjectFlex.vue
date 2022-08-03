<template>
  <div class="single-item" v-for="project in projects" :key="project">
    <ProjectSingle
      :description="project.description"
      :video="project.video"
      :url="project.url"
      :isRectangle="true"
      :framework="project.framework"
      :title="project.title"
    />
  </div>
</template>

<script>
import ProjectSingle from "./ProjectSingle.vue";
export default {
  data() {
    return {
      projects: [
        {
          framework: "VUE.JS",
          date: "July 22, 2022",
          status: "Online",
          title: "API Dog App",
          description: "Random Dog App with images",
          video: "Click here",
          url: "https://infinitedogapp.netlify.app",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Online",
          framework: "HTML, CSS, & JAVASCRIPT",
          title: "Adeori Resturant",
          description: "Resturant design with sticky header",
          video: "Click here",
          url: "https://adeori-resturant.netlify.app/",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Online",
          framework: "VUE.JS",
          title: "LocaHost Chat rooms",
          description: "Local Host Chat Rooms",
          video: "Click here",
          url: "https://localhostchatrooms.netlify.app/",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Online",
          framework: "VUE.JS",
          title: "JUNGIAN ARCHETYPE QUIZ",
          description:
            "Free Archetype Quiz Reveals Your Personality Quirks, Innate Talents, and Hidden Weaknesses!",
          video: "Click here",
          url: "https://archytype-quiz.netlify.app/",
          slides: "Slides",
        },
      ],
    };
  },
  components: { ProjectSingle },
};
</script>

<style scoped>
.single-item {
  margin-bottom: 10px;
}
@media (max-width: 380px) {
  .single-item {
    margin-top: 10px;
  }
}
</style>
