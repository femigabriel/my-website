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
          url: "adeori-resturant.netlify.app",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Online",
          framework: "Vue.JS",
          title: "JUNGIAN ARCHETYPE QUIZ",
          description: "JUNGIAN ARCHETYPE QUIZ",
          video: "Click here",
          url: "archytype-quiz.netlify.app",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Online",
          framework: "VUE.JS",
          title: "APPRUV ACCOUNT",
          description: "Create a new account",
          video: "Click here",
          url: "aprruve.netlify.app",
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
</style>
