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
          framework: "JAVASCRIPT",
          title: "Random Jokes",
          description: "Random jokes that will crack you up!",
             video: "Click here",
          url: "https://trusting-yalow-1c4467.netlify.app",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Online",
          framework: "JAVASCRIPT",
          title: "Random Jokes",
          description: "Random jokes that will crack you up!",
            video: "Click here",
          url: "https://trusting-yalow-1c4467.netlify.app",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Online",
          framework: "JAVASCRIPT",
          title: "Random Jokes",
          description: "Random jokes that will crack you up!",
             video: "Click here",
          url: "https://trusting-yalow-1c4467.netlify.app",
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
